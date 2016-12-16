require 'yaml'

task :generate do
  maps = YAML.load_file '_data/maps.yml'
  maps.each do |map|
    File.open "maps/#{map['slug']}.html", 'w' do |f|
      f.write <<HTML
---
layout: default
---
<div class="map">
  <a href="..">
    <img src=../img/#{map['img']} />
  </a>
</div>
HTML
    end
  end
end
