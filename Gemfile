# frozen_string_literal: true

source "https://rubygems.org"

gem "cocoapods"
gem "cocoapods-binary"
gem "fastlane"
gem "slather"

gem "badge"

gem "xcode-install"
gem "bundle-audit"

plugins_path = File.join(File.dirname(__FILE__), 'fastlane', 'Pluginfile')
eval_gemfile(plugins_path) if File.exist?(plugins_path)
