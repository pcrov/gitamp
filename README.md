# GitAmp

[![Build Status](https://travis-ci.org/ekinhbayar/gitamp.svg?branch=master)](https://travis-ci.org/ekinhbayar/gitamp)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/ekinhbayar/gitamp/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/ekinhbayar/gitamp/?branch=master)
[![Code Coverage](https://scrutinizer-ci.com/g/ekinhbayar/gitamp/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/ekinhbayar/gitamp/?branch=master)
[![Code Climate](https://codeclimate.com/github/ekinhbayar/gitamp/badges/gpa.svg)](https://codeclimate.com/github/ekinhbayar/gitamp)

Listen to music generated by events across github.

Made with [amphp](http://amphp.org/) magic `<3`

Clone of [github.audio](https://github.audio).

Requires:

 - PHP 7

## Usage

- Run `composer install`
- Copy the config.sample.php file and change the settings
- Run the server using `vendor/bin/aerys -c server.php`
- Open your browser and go to http://localhost:1337 (for default settings)
- Profit!

## Development

- Run the server using `vendor/bin/aerys -c server.php -d` for debugging output

## GitAmp as a Service

To run GitAmp as a systemd unit:

- Copy the [gitamp.sample.service](https://github.com/ekinhbayar/gitamp/blob/master/gitamp.sample.service) to `/etc/systemd/system/gitamp.service`.
- Replace the paths with your installation location.
- Enable it by running `systemctl enable gitamp` && start with `systemctl start gitamp`

If you want to run it after reboots as well, symlink the service file under `multi-user.target.wants` via 

`ln -sf /etc/systemd/system/gitamp.service /etc/systemd/system/multi-user.target.wants/gitamp.service`

## Optional Dependencies

For true non-blocking execution, install one of the following:

- [`libevent`](https://pecl.php.net/package/libevent) PECL extension.
- [`ev`](https://pecl.php.net/package/ev) PECL extension
- [`php-uv`](https://github.com/bwoebi/php-uv) PHP extension.

## Issues

All features requests, bug reports or questions can be posted in [GitHub issues](https://github.com/ekinhbayar/gitamp/issues).

For security related reports please send a mail to gitamp-security@pieterhordijk.com instead of using GitHub's issues.
