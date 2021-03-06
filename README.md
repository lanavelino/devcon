![image](https://raw.github.com/devcon-ph/devcon/master/app/assets/images/logo.png)

# DevCon

This is a work-in-progress revamp for the website of [Developers Connnect Philippines](http://devcon.ph)

## Developer Notes

This is a run of the mill Rails + PostgreSQL app so running a local copy should look something like:

    git clone git://github.com/devcon-ph/devcon.git
    cd devcon
    bundle
    cp config/database.yml.example config/database.yml
    vim config/database.yml
    rake db:create
    rake db:migrate
    guard

Guard will run both the Unicorn server at port 3000 and the specs.

This app uses [better\_errors](https://github.com/charliesome/better_errors) for debugging. Don't forget to set the `TRUSTED_IP` environment variable if you're not testing on your local machine.

This app also uses [rails\_panel](https://github.com/dejan/rails_panel) so you don't need to look at the development log while developing.

## Plans

All future enhancements are logged at https://github.com/devcon-ph/devcon/issues. Anyone may fork this project and provide pull requests related to those enhancements.

## Deployment

This app has two main branches, the `master` branch for staging i.e. http://beta.devcon.ph, and the `release` branch for production i.e. http://devcon.ph. All enhancements must be performed on the `master` branch and tested prior to merging to the `release` branch.

As of this writing, only [Bry](https://github.com/bryanbibat/) and [Terence](https://github.com/terenceponce) have access rights to deploy to the server.
