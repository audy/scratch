#!/usr/bin/env ruby

# remove `focus: true` from RSpec tests

Dir['spec/**/*.rb'].each do |file|
  orig = File.read(file)
  count = 0
  changed = orig.gsub(/, focus: true/) { count += 1; '' }

  if changed != orig
    puts "#{file} -> #{count} change(s)"
    File.open(file, 'w') do |handle|
      handle.write(changed)
    end
  end
end
