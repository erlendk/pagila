
# Init and load repository into github.com

    git init
    git add README.md pagila-0.10.1
    git commit -m "Init."
    git remote add origin git@github.com:sdoro/pagila.git
    git push -u origin master

    # make storyboard.md
    git add storyboard.md
    git commit -m "Add storyboard.md"
    git push

# Init Heroku side

    # make a heroku account
    # push "create a database" button
    # zuccante-2015-16 :: silver :: postgresql-sinuous-6778
    heroku login # type e-mail/password
    heroku pg:psql --app zuccante-2015-16 HEROKU_POSTGRESQL_SILVER < pagila-0.10.1/pagila-schema.sql

