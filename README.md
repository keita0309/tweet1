# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

## user テーブル
|Column|Type|Options|
|------|----|-------|
|id|integet|
|email|string|
|password|string|
|username|string|
|nickname|string|

- has_many :tweets
- has_many :comments

## tweetテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|
|image|string|
|text|string|
|user_id|integer|

### Association
- belongs_to :user
- has_many :comments

## comment テーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integet|
|tweet_id|text|
|text|text|

- belongs_to :tweet
- belongs_to :user
