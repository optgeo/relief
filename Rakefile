desc 'create tiles from Natural Earth II'
task :tiles do
  sh "docker run -ti --rm -v /Users/hfu/Downloads:/mnt/downloads -v /Users/hfu/relief:/mnt/relief osgeo/gdal gdal2tiles.py -z 0-5 --xyz --tilesize=512 --webviewer=leaflet /mnt/downloads/NE2_HR_LC_SR_W_DR/NE2_HR_LC_SR_W_DR.tif /mnt/relief/docs/zxy"
end

desc 'create style.json'
task :style do
  sh 'parse-hocon hocon/style.conf > docs/style.json'
  sh 'gl-style-validate docs/style.json'
end

desc 'host the site for testing'
task :host do
  sh 'budo -d docs'
end

