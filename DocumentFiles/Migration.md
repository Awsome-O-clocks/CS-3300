# Migrations

## Resourses
[Django Migration Documentation](https://docs.djangoproject.com/en/4.2/topics/migrations/)

## Table of contents
- 

When you need to commit a change in your models into django you must make a migration.
Migrations are a form of version contol. When you make a change to your models migration is how you will apply them.

To find your migrations go into your project folder and under the migrations folder you will see your models builds. All of your migrations will go here and are meant to be distibuted as needed.

Changes are made semi automaticly. When you change a model a migration will need to be done manualy. When you make an instance of a model the change to the database will be made automaticly. When you make a new model or make a new/delete a feild in the model you need to run the `makemigration` command and then the `migrate` command.


# Reversing a Migration
You can run the `showmigration` command to look for the migration numbers. This will be usefull for telling django which migtration you want to reverse.

Then you can run this command to reverse.
```
python manage.py migrate <project> <migrationID>
```

If you need to reverse all migration then run `zero` as the migration ID.


## Errors
There may be an intance where you get the IrreversibleError this is due to the migration containing irreversible opperations.


# Commands List
`migrate` - solidifies the changes and applies them to the database.
`makemigrations` - packs up your models and turns them into individual migration files. Remember to read the output from this command as it may not detect the changes you want to make correctly.
`sqlmigrate`
`showmigrations`

Each of these commands are run with the form:
```
python manage.py <command>
```


# Things of Note

### Removing a model feild
If you decide to remove a feild while there are still refrences to said feild then that will cause issuse.
The System_check_deprecated_details attribute will give a msg when using a deleted feild.
This should be changed to System_check_removed_details after a few releases.

### Data migrations
These are not Automatic if you goto the first link in the [resourses heading](#Resourses) you can find more information on how to do this.

These types of migrations in django are made up of Opperations. RunPython is the most used example of these opperations.

