# テクノロジー（藤原）12/6授業

## Bashの実行ログ

```
fukuzaki93:~/workspace/lecture-1206/asagao (master) $ bin/rails g model member
      invoke  active_record
      create    db/migrate/20171206003319_create_members.rb
      create    app/models/member.rb
fukuzaki93:~/workspace/lecture-1206/asagao (master) $ bin/rails db:migrate
Error: Command 'db:migrate' not recognized
/usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:151:in `write_error_message': undefined method `success?' for nil:NilClass (NoMethodError)
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:41:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
fukuzaki93:~/workspace/lecture-1206/asagao (master) $ bin/rails c
Loading development environment (Rails 4.2.10)
2.4.0 :001 > Member.count
ActiveRecord::StatementInvalid: Could not find table 'members'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/activerecord-4.2.10/lib/active_record/connection_adapters/sqlite3_adapter.rb:501:in `table_structure'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/activerecord-4.2.10/lib/active_record/connection_adapters/sqlite3_adapter.rb:375:in `columns'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/activerecord-4.2.10/lib/active_record/connection_adapters/schema_cache.rb:43:in `columns'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/activerecord-4.2.10/lib/active_record/attributes.rb:93:in `columns'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/activerecord-4.2.10/lib/active_record/model_schema.rb:260:in `column_names'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/activerecord-4.2.10/lib/active_record/relation/calculations.rb:232:in `aggregate_column'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/activerecord-4.2.10/lib/active_record/relation/calculations.rb:258:in `execute_simple_calculation'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/activerecord-4.2.10/lib/active_record/relation/calculations.rb:227:in `perform_calculation'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/activerecord-4.2.10/lib/active_record/relation/calculations.rb:133:in `calculate'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/activerecord-4.2.10/lib/active_record/relation/calculations.rb:48:in `count'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/activerecord-4.2.10/lib/active_record/querying.rb:13:in `count'
        from (irb):1
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :002 > 
2.4.0 :003 >   exit
fukuzaki93:~/workspace/lecture-1206/asagao (master) $ bin/rake db:migrate
== 20171206003319 CreateMembers: migrating ====================================
-- create_table(:members)
   -> 0.0017s
== 20171206003319 CreateMembers: migrated (0.0018s) ===========================

fukuzaki93:~/workspace/lecture-1206/asagao (master) $ bin/rails c
Loading development environment (Rails 4.2.10)
2.4.0 :001 > Member:count
NoMethodError: undefined method `Member' for main:Object
        from (irb):1
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :002 > Member:count
NoMethodError: undefined method `Member' for main:Object
        from (irb):2
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :003 > ^C
2.4.0 :003 > q
NameError: undefined local variable or method `q' for main:Object
        from (irb):3
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :004 > exit
fukuzaki93:~/workspace/lecture-1206/asagao (master) $ bin/rake db:migrate
fukuzaki93:~/workspace/lecture-1206/asagao (master) $ bin/rails c
Loading development environment (Rails 4.2.10)
2.4.0 :001 > 
2.4.0 :002 >   Member.count
   (0.1ms)  SELECT COUNT(*) FROM "members"
 => 0 
2.4.0 :003 > member = Member.new
 => #<Member id: nil, number: nil, name: nil, full_name: nil, email: nil, birthday: nil, gender: 0, administrator: false, created_at: nil, updated_at: nil> 
2.4.0 :004 > member = 1
 => 1 
2.4.0 :005 > member.number = 1                                 
NoMethodError: undefined method `number=' for 1:Integer
        from (irb):5
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :006 > member.number = 1
NoMethodError: undefined method `number=' for 1:Integer
        from (irb):6
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :007 > member = Member.new
 => #<Member id: nil, number: nil, name: nil, full_name: nil, email: nil, birthday: nil, gender: 0, administrator: false, created_at: nil, updated_at: nil> 
2.4.0 :008 > member.number = 1
 => 1 
2.4.0 :009 > member.name = "Taro"
 => "Taro" 
2.4.0 :010 > member.save
   (0.1ms)  begin transaction
  SQL (0.4ms)  INSERT INTO "members" ("number", "name", "created_at", "updated_at") VALUES (?, ?, ?, ?)  [["number", 1], ["name", "Taro"], ["created_at", "2017-12-06 00:44:33.813142"], ["updated_at", "2017-12-06 00:44:33.813142"]]
   (9.4ms)  commit transaction
 => true 
2.4.0 :011 > Member.first
  Member Load (0.4ms)  SELECT  "members".* FROM "members"  ORDER BY "members"."id" ASC LIMIT 1
 => #<Member id: 1, number: 1, name: "Taro", full_name: nil, email: nil, birthday: nil, gender: 0, administrator: false, created_at: "2017-12-06 00:44:33", updated_at: "2017-12-06 00:44:33"> 
2.4.0 :012 > pp Member.first
  Member Load (0.4ms)  SELECT  "members".* FROM "members"  ORDER BY "members"."id" ASC LIMIT 1
#<Member:0x00000003aab768
 id: 1,
 number: 1,
 name: "Taro",
 full_name: nil,
 email: nil,
 birthday: nil,
 gender: 0,
 administrator: false,
 created_at: Wed, 06 Dec 2017 09:44:33 JST +09:00,
 updated_at: Wed, 06 Dec 2017 09:44:33 JST +09:00>
 => #<Member id: 1, number: 1, name: "Taro", full_name: nil, email: nil, birthday: nil, gender: 0, administrator: false, created_at: "2017-12-06 00:44:33", updated_at: "2017-12-06 00:44:33"> 
2.4.0 :013 > member = Member.first
  Member Load (0.3ms)  SELECT  "members".* FROM "members"  ORDER BY "members"."id" ASC LIMIT 1
 => #<Member id: 1, number: 1, name: "Taro", full_name: nil, email: nil, birthday: nil, gender: 0, administrator: false, created_at: "2017-12-06 00:44:33", updated_at: "2017-12-06 00:44:33"> 
2.4.0 :014 > membe.number = 41
NameError: undefined local variable or method `membe' for main:Object
Did you mean?  member
        from (irb):14
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :015 > member.number = 41                                
 => 41 
2.4.0 :016 > member = Member.first                             
  Member Load (0.3ms)  SELECT  "members".* FROM "members"  ORDER BY "members"."id" ASC LIMIT 1
 => #<Member id: 1, number: 1, name: "Taro", full_name: nil, email: nil, birthday: nil, gender: 0, administrator: false, created_at: "2017-12-06 00:44:33", updated_at: "2017-12-06 00:44:33"> 
2.4.0 :017 > member.number = 41                                
 => 41 
2.4.0 :018 > member.save
   (0.1ms)  begin transaction
  SQL (0.3ms)  UPDATE "members" SET "number" = ?, "updated_at" = ? WHERE "members"."id" = ?  [["number", 41], ["updated_at", "2017-12-06 00:46:13.449719"], ["id", 1]]
   (9.0ms)  commit transaction
 => true 
2.4.0 :019 > Member.first
  Member Load (0.3ms)  SELECT  "members".* FROM "members"  ORDER BY "members"."id" ASC LIMIT 1
 => #<Member id: 1, number: 41, name: "Taro", full_name: nil, email: nil, birthday: nil, gender: 0, administrator: false, created_at: "2017-12-06 00:44:33", updated_at: "2017-12-06 00:46:13"> 
2.4.0 :020 > 
fukuzaki93:~/workspace/lecture-1206/asagao (master) $ mkdir -p db/seeds/development
fukuzaki93:~/workspace/lecture-1206/asagao (master) $ touch db/seeds/development/members.rb
fukuzaki93:~/workspace/lecture-1206/asagao (master) $ bin/rake db:reset
-- create_table("members", {:force=>:cascade})
   -> 0.0147s
-- initialize_schema_migrations_table()
   -> 0.0365s
-- create_table("members", {:force=>:cascade})
   -> 0.0090s
-- initialize_schema_migrations_table()
   -> 0.0147s
Creating members...
fukuzaki93:~/workspace/lecture-1206/asagao (master) $ bin/rake db:seed
Creating members...
fukuzaki93:~/workspace/lecture-1206/asagao (master) $ bin/rails c
Loading development environment (Rails 4.2.10)
2.4.0 :001 > pp Member.first
  Member Load (0.2ms)  SELECT  "members".* FROM "members"  ORDER BY "members"."id" ASC LIMIT 1
#<Member:0x0000000355c6e0
 id: 1,
 number: 10,
 name: "Taro",
 full_name: "佐藤 太郎",
 email: "Taro@example.com",
 birthday: Tue, 01 Dec 1981,
 gender: 0,
 administrator: true,
 created_at: Wed, 06 Dec 2017 09:51:44 JST +09:00,
 updated_at: Wed, 06 Dec 2017 09:51:44 JST +09:00>
 => #<Member id: 1, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 00:51:44", updated_at: "2017-12-06 00:51:44"> 
2.4.0 :002 > 
fukuzaki93:~/workspace/lecture-1206/asagao (master) $ bin/rails db
SQLite version 3.8.2 2013-12-06 14:53:30
Enter ".help" for instructions
Enter SQL statements terminated with a ";"
sqlite> .tables
members            schema_migrations
sqlite> .schema members
CREATE TABLE "members" ("id" INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL, "number" integer NOT NULL, "name" varchar NOT NULL, "full_name" varchar, "email" varchar, "birthday" date, "gender" integer DEFAULT 0 NOT NULL, "administrator" boolean DEFAULT 'f' NOT NULL, "created_at" datetime NOT NULL, "updated_at" datetime NOT NULL);
sqlite> SELECT * from members;
1|10|Taro|佐藤 太郎|Taro@example.com|1981-12-01|0|t|2017-12-06 00:51:44.845157|2017-12-06 00:51:44.845157
2|11|Jiro|鈴木 次郎|Jiro@example.com|1981-12-01|0|f|2017-12-06 00:51:44.859106|2017-12-06 00:51:44.859106
3|12|Hana|高橋 花子|Hana@example.com|1981-12-01|1|f|2017-12-06 00:51:44.867051|2017-12-06 00:51:44.867051
4|13|John|田中 太郎|John@example.com|1981-12-01|0|f|2017-12-06 00:51:44.877627|2017-12-06 00:51:44.877627
5|14|Mike|佐藤 次郎|Mike@example.com|1981-12-01|0|f|2017-12-06 00:51:44.887040|2017-12-06 00:51:44.887040
6|15|Sophy|鈴木 花子|Sophy@example.com|1981-12-01|1|f|2017-12-06 00:51:44.896726|2017-12-06 00:51:44.896726
7|16|Bill|高橋 太郎|Bill@example.com|1981-12-01|0|f|2017-12-06 00:51:44.905423|2017-12-06 00:51:44.905423
8|17|Alex|田中 次郎|Alex@example.com|1981-12-01|0|f|2017-12-06 00:51:44.913667|2017-12-06 00:51:44.913667
9|18|Mary|佐藤 花子|Mary@example.com|1981-12-01|1|f|2017-12-06 00:51:44.921575|2017-12-06 00:51:44.921575
10|19|Tom|鈴木 太郎|Tom@example.com|1981-12-01|0|f|2017-12-06 00:51:44.929550|2017-12-06 00:51:44.929550
11|10|Taro|佐藤 太郎|Taro@example.com|1981-12-01|0|t|2017-12-06 00:51:56.096417|2017-12-06 00:51:56.096417
12|11|Jiro|鈴木 次郎|Jiro@example.com|1981-12-01|0|f|2017-12-06 00:51:56.106428|2017-12-06 00:51:56.106428
13|12|Hana|高橋 花子|Hana@example.com|1981-12-01|1|f|2017-12-06 00:51:56.171813|2017-12-06 00:51:56.171813
14|13|John|田中 太郎|John@example.com|1981-12-01|0|f|2017-12-06 00:51:56.182557|2017-12-06 00:51:56.182557
15|14|Mike|佐藤 次郎|Mike@example.com|1981-12-01|0|f|2017-12-06 00:51:56.191105|2017-12-06 00:51:56.191105
16|15|Sophy|鈴木 花子|Sophy@example.com|1981-12-01|1|f|2017-12-06 00:51:56.201229|2017-12-06 00:51:56.201229
17|16|Bill|高橋 太郎|Bill@example.com|1981-12-01|0|f|2017-12-06 00:51:56.209801|2017-12-06 00:51:56.209801
18|17|Alex|田中 次郎|Alex@example.com|1981-12-01|0|f|2017-12-06 00:51:56.219127|2017-12-06 00:51:56.219127
19|18|Mary|佐藤 花子|Mary@example.com|1981-12-01|1|f|2017-12-06 00:51:56.229240|2017-12-06 00:51:56.229240
20|19|Tom|鈴木 太郎|Tom@example.com|1981-12-01|0|f|2017-12-06 00:51:56.237669|2017-12-06 00:51:56.237669
sqlite> .quit
fukuzaki93:~/workspace/lecture-1206/asagao (master) $ bin/rails c
Loading development environment (Rails 4.2.10)
2.4.0 :001 > Member.ids
   (0.2ms)  SELECT "members"."id" FROM "members"
 => [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20] 
2.4.0 :002 > member = Members.find(3)
NameError: uninitialized constant Members
        from (irb):2
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :003 > member = Member.find(3)
  Member Load (0.3ms)  SELECT  "members".* FROM "members" WHERE "members"."id" = ? LIMIT 1  [["id", 3]]
 => #<Member id: 3, number: 12, name: "Hana", full_name: "高橋 花子", email: "Hana@example.com", birthday: "1981-12-01", gender: 1, administrator: false, created_at: "2017-12-06 00:51:44", updated_at: "2017-12-06 00:51:44"> 
2.4.0 :004 > member.email
 => "Hana@example.com" 
2.4.0 :005 > member = Member.find_by(name: "Taro")
  Member Load (0.3ms)  SELECT  "members".* FROM "members" WHERE "members"."name" = ? LIMIT 1  [["name", "Taro"]]
 => #<Member id: 1, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 00:51:44", updated_at: "2017-12-06 00:51:44"> 
2.4.0 :006 > member = Member.find_by(gender: 0,administrator: false)
  Member Load (0.3ms)  SELECT  "members".* FROM "members" WHERE "members"."gender" = ? AND "members"."administrator" = ? LIMIT 1  [["gender", 0], ["administrator", "f"]]
 => #<Member id: 2, number: 11, name: "Jiro", full_name: "鈴木 次郎", email: "Jiro@example.com", birthday: "1981-12-01", gender: 0, administrator: false, created_at: "2017-12-06 00:51:44", updated_at: "2017-12-06 00:51:44"> 
2.4.0 :007 > member = Member.find_by(gender 1, administrator: true)
NoMethodError: undefined method `gender' for main:Object
        from (irb):7
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :008 > member = Member.find_by(gender: 1, administrator: true)  
  Member Load (0.2ms)  SELECT  "members".* FROM "members" WHERE "members"."gender" = ? AND "members"."administrator" = ? LIMIT 1  [["gender", 1], ["administrator", "t"]]
 => nil 
2.4.0 :009 > member = Member.where(name: "Taro")
  Member Load (0.4ms)  SELECT "members".* FROM "members" WHERE "members"."name" = ?  [["name", "Taro"]]
 => #<ActiveRecord::Relation [#<Member id: 1, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 00:51:44", updated_at: "2017-12-06 00:51:44">, #<Member id: 11, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 00:51:56", updated_at: "2017-12-06 00:51:56">]> 
2.4.0 :010 > puts member.to_sql
SELECT "members".* FROM "members" WHERE "members"."name" = 'Taro'
 => nil 
2.4.0 :011 > members = Member.where(name: "Taro")
  Member Load (0.2ms)  SELECT "members".* FROM "members" WHERE "members"."name" = ?  [["name", "Taro"]]
 => #<ActiveRecord::Relation [#<Member id: 1, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 00:51:44", updated_at: "2017-12-06 00:51:44">, #<Member id: 11, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 00:51:56", updated_at: "2017-12-06 00:51:56">]> 
2.4.0 :012 > members = member.where("number < 20")
  Member Load (0.4ms)  SELECT "members".* FROM "members" WHERE "members"."name" = ? AND (number < 20)  [["name", "Taro"]]
 => #<ActiveRecord::Relation [#<Member id: 1, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 00:51:44", updated_at: "2017-12-06 00:51:44">, #<Member id: 11, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 00:51:56", updated_at: "2017-12-06 00:51:56">]> 
2.4.0 :013 > members = Member.where(name: "Taro").where("number < 20")
  Member Load (0.2ms)  SELECT "members".* FROM "members" WHERE "members"."name" = ? AND (number < 20)  [["name", "Taro"]]
 => #<ActiveRecord::Relation [#<Member id: 1, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 00:51:44", updated_at: "2017-12-06 00:51:44">, #<Member id: 11, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 00:51:56", updated_at: "2017-12-06 00:51:56">]> 
2.4.0 :014 > ,e,bers =Member.where(gender: 1).order("number")
SyntaxError: (irb):14: syntax error, unexpected ','
,e,bers =Member.where(gender: 1
 ^
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :015 > members =Member.where(gender: 1).order("number")         
  Member Load (0.4ms)  SELECT "members".* FROM "members" WHERE "members"."gender" = ?  ORDER BY number  [["gender", 1]]
 => #<ActiveRecord::Relation [#<Member id: 3, number: 12, name: "Hana", full_name: "高橋 花子", email: "Hana@example.com", birthday: "1981-12-01", gender: 1, administrator: false, created_at: "2017-12-06 00:51:44", updated_at: "2017-12-06 00:51:44">, #<Member id: 13, number: 12, name: "Hana", full_name: "高橋 花子", email: "Hana@example.com", birthday: "1981-12-01", gender: 1, administrator: false, created_at: "2017-12-06 00:51:56", updated_at: "2017-12-06 00:51:56">, #<Member id: 6, number: 15, name: "Sophy", full_name: "鈴木 花子", email: "Sophy@example.com", birthday: "1981-12-01", gender: 1, administrator: false, created_at: "2017-12-06 00:51:44", updated_at: "2017-12-06 00:51:44">, #<Member id: 16, number: 15, name: "Sophy", full_name: "鈴木 花子", email: "Sophy@example.com", birthday: "1981-12-01", gender: 1, administrator: false, created_at: "2017-12-06 00:51:56", updated_at: "2017-12-06 00:51:56">, #<Member id: 9, number: 18, name: "Mary", full_name: "佐藤  花子", email: "Mary@example.com", birthday: "1981-12-01", gender: 1, administrator: false, created_at: "2017-12-06 00:51:44", updated_at: "2017-12-06 00:51:44">, #<Member id: 19, number: 18, name: "Mary", full_name: "佐藤 花子", email: "Mary@example.com", birthday: "1981-12-01", gender: 1, administrator: false, created_at: "2017-12-06 00:51:56", updated_at: "2017-12-06 00:51:56">]> 
2.4.0 :016 > 
```