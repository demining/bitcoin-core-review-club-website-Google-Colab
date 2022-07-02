# bitcoin-core-review-club


-------------------------
### Run Google-Colab

https://colab.research.google.com/drive/1OShIMVcFZ_khsUIBOIV1lzrqAGo1gfm_?usp=sharing

-------------------------


Simple Jekyll site for hosting the Bitcoin Core PR Review club at https://bitcoincore.reviews/.

## Development

You'll need [Ruby and Jekyll](https://jekyllrb.com/docs/installation/) to run
the site locally. Ruby 2.6 is recommended. Once they are set up:

* Clone the repository and go into the directory
* Run `bundle install`
* Run `make preview`
* Go to http://localhost:4000

In case of any issues, don't hesitate to run the following to update rubygems,
bundler, and dependencies: `gem update --system && gem update && bundle update`

## Making a new post

See the [CONTRIBUTING.md](CONTRIBUTING.md) doc for how to create a post for an upcoming meeting.

## Changing Site Data

All site configurations are either contained in `_config.yml` or `_data/settings.yml`. Some data is duplicated between the two due to the way Jekyll injects variables, so be sure to update both.

## Running the Test Suite

To run all tests: `rake test` or just `rake`

To run one test file: `rake TEST=test/test_rake_posts_new`

To run an individual test in a test file:
`rake TEST=test/test_rake_posts_new TESTOPTS=--name=test_rake_posts_new`

Before running tests for the first time, you may need to run `bundle update`.

Before running the `test_all_links` test (or all of the tests, which includes
it), the site needs to be started up locally with `make preview`, or with `make
clean preview` if any meeting logs were changed, to pre-render the logs through
the `auto_logs_markup` plugin.

## Attributions

Thanks to [LeNPaul](https://github.com/LeNPaul/jekyll-starter-kit) for the Jekyll starter kit this was forked from and to Will O'Beirne for pointing me in that direction.

----

|  | Donation Address |
| --- | --- |
| ♥ __BTC__ | 1Lw2kh9WzCActXSGHxyypGLkqQZfxDpw8v |
| ♥ __ETH__ | 0xaBd66CF90898517573f19184b3297d651f7b90bf |
