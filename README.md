# Sambal

Sambal is a ruby samba client

Quite a bit of code was borrowed from https://github.com/reivilo/rsmbclient - Thanks!

## Installation

Add this line to your application's Gemfile:

    gem 'sambal'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install sambal

## Usage

    client = Sambal::Client.new(domain: 'WORKGROUP', host: '127.0.0.1', share: '', user: 'guest', password: '--no-pass', port: 445)
    client.ls # returns hash of files
    client.put("local_file.txt","remote_file.txt") # uploads file to server
    client.put_content("My content here", "remote_file") # uploads content to a file on server
    client.get("remote_file.txt", "local_file.txt") # downloads file from server
    client.delete("remote_file.txt") # deletes files from server
    client.cd("some_directory") # changes directory on server
    client.close # closes connection

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request