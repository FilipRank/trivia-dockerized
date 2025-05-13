FROM mongo:8.0.4
COPY my_dump /dump
CMD ["sh", "-c", "mongod --fork --logpath /var/log/mongodb.log --dbpath /data/db && mongorestore --host localhost --db trivia-app /dump/trivia-app && mongod --shutdown && exec mongod --bind_ip_all"]