FROM ruby:3.2.2

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs default-mysql-client vim
# RailsのインストールやMySQLへの接続に必要なパッケージをインストール

RUN mkdir /api
# コンテナ内にapiディレクトリを作成

WORKDIR /api
# 作成したapiディレクトリを作業用ディレクトリとして設定

COPY Gemfile /api/Gemfile
COPY Gemfile.lock /api/Gemfile.lock
# ローカルの Gemfile と Gemfile.lock をコンテナ内のapi配下にコピー

RUN bundle install
# コンテナ内にコピーした Gemfile の bundle install

COPY . /api
# ローカルの同階層のファイルをコンテナ内のapi配下にコピー

CMD ["rails", "server", "-b", "0.0.0.0"]
