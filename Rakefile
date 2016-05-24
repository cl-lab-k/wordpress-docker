require 'rake'

$PROJECT_ROOT = File.expand_path( __dir__ )
ENV['MACHINE_STORAGE_PATH']=File.join( $PROJECT_ROOT, '.docker', 'machine' )

task :default => [
  :create,
  :up,
]

task :create do
  if not File.exists?( File.join( $PROJECT_ROOT, '.docker', 'machine',
                                  'machines', 'wordpress' ) )
    sh <<-_EOF_
docker-machine create \
	--driver virtualbox \
	--virtualbox-memory=8192 \
	--virtualbox-cpu-count=2 \
	wordpress
    _EOF_
  end
end

task :up do
  sh <<-_EOF_
eval $(docker-machine env wordpress) && \
docker-compose -p wordpress up -d
  _EOF_
end

task :rebuild do
  sh <<-_EOF_
eval $(docker-machine env wordpress) && \
docker-compose -p wordpress build
  _EOF_
end

task :rm do
  sh <<-_EOF_
eval $(docker-machine env wordpress) && \
docker-machine rm wordpress
  _EOF_
end
