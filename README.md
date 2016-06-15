# SportsBlog                        <br>
 <br>
<img src='https://github.com/kosomi/SportsBlog/blob/master/Untitled.png'>                        <br>
 <br>
Create the text file gitignore.txt.                        <br>               
Open it in a text editor and add your rules, then save and close.                        <br>                    
Hold SHIFT, right click the folder you're in, then select Open command window here.                        <br>
Then rename the file in the command line, with ren gitignore.txt .gitignore.                        <br>
       <br>
       <br>
1. MongDB 설치 (mongodb.org/downloads)       <br>
       <br>
2. bin> mongod --directoryperdb --dbpath c:/mongodb/data/db --logpath c:/mongodb/log/mongo.log --logappend --rest --install       <br>
       <br>
3 bin> net start mongoDB       <br>
the MongoDb service was started successfully       <br>
       <br>
4. bin> mongo (엔터) 실행       <br>
welcome to the mongoDB shell       <br>
       <br>
5. MongoDB commands       <br>
show databases, use..        <br>
       <br>
6 Express generator 실행       <br>
ex) express sportblog       <br>
       <br>
7. Package.json 디펜던시 추가       <br>
express-session, express-validator, express-messages, connect-flash, moment, mongoose       <br>
"main":"bin/www"       <br>
       <br>
8 express-session 추가       <br>
9 express-validator       <br>
10. express-messages       <br>
       <br>
var session = require('express-session');       <br>
express-validator       <br>
connect-flash       <br>
       <br>
11. app.js에 몽구스 추가 (mongoose.js 참조)       <br>
var mongoose = require('mongoose');       <br>
mongoose.connect('mongodb://localhost/sportblog');       <br>
var db = mongoose.connection;       <br>
       <br>
12 startbootstrap.com 애서 하나 받기       <br>
필요한 assets 옮기기, layout에서 필요한것 jade로 변환 후 복붙.       <br>
       <br>
13 includes 폴더 만든 후 navbar.js 인크루드하기       <br>
include ./includes/navbar.jade       <br>
       <br>
14. 라우트       <br>
var route = require('./routes/index');       <br>
var article = require('./routes/article');       <br>
var categories = require('./routes/categories');       <br>
var manage = require('./routes/manage');       <br>
       <br>
app.use('/', routes);       <br>
app.use('/articles', articles);       <br>
       <br>
15 views에 파일 생성       <br>
       <br>
16 article, articles.jade 정리, post 복붙       <br>
       <br>
17 Mongoose       <br>
       <br>
app.js       <br>
var mongoose = require('mongoose');       <br>
mongoose.connect('mongodb://localhost/sportsblog');       <br>
var db = mongoose.connection;       <br>
       <br>
models/article.js       <br>
var mongoose = require('mongoose');       <br>
var articleSchema = mongoose.schema({});       <br>
       <br>
(compile command) 컴파일     <br>
var Article = module.exports = mongoose.model(Article, articleSchema);       <br>
Article.find(query.call).limit(limit);       <br>
       <br>
index.js       <br>
Article = require('../modles/article.js')       <br>
Route.get('/',function(req,res,next){       <br>
Article.getArticles(function(err,articles){res.render(index,{title:'express',articles:articles})});       <br>
       <br>
18 moment 시간표시       <br>
app.locals.moment = require('moment');       <br>






















