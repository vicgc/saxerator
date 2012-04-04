# More info at https://github.com/guard/guard#readme

guard :bundler do
  watch('Gemfile')
  watch(/^saxerator\.gemspec$/)
end

guard :rspec, :cli => '--color --format doc' do
  watch(%r{^spec/.+_spec\.rb$})
  watch(%r{^lib/(.+)\.rb$})     { |m| "spec/lib/#{m[1]}_spec.rb" }
  watch('spec/spec_helper.rb')  { "spec" }
end