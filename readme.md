#### install
    install python 2.7

#### thư viện python

    https://github.com/fananimi/pyzk
    https://github.com/AlSayedGamal/python_zklib

#### install postgresql
    sudo apt-get install postgresql
    sudo -i -u postgres
    psql
    sudo -u postgres psql postgres
    \password postgres
    
    docker run --name TechDB -e POSTGRES_PASSWORD=123 -d -p 5432:5432 postgres:latest
	-----
    docker exec -it -u postgres FingerDB psql
    
	-----
    create table datatable (
    numerical serial primary key not null,
    iduser int not null,
    name text not null,
    date date not null,
    time time not null,
    method_swipe int not null);
    -----
    create table usertable (
    uid int primary key not null,
    iduser int not null,
    name text not null, 
    privilege text,
    password text,
    groupid text);
    ---------------------------
    create table timetable (
    numerical serial primary key not null,
    iduser int not null,
    name text not null,
    date date,
    timein time,
    timeout time,
    timelate time,
    timeearly time);

----------
#### install flask and pip
    sudo apt install python-pip	    # python 2
    sudo apt install python3-pip	# python 3
    sudo pip install flask          
    sudo pip install wtforms
    sudo pip install psycopg2       # Read database
    sudo pip install psycopg2-binary
    sudo pip install Flask-SQLALchemy


----------
#### Run App
    git clone https://github.com/long25vn/fingerprint_scanner_python.git
    cd fingerprint_scanner_python/
    python pulldata.py
    python pulluser.py
    python control.py

file pushdata chạy liên tục để đẩy dữ liệu trên máy chấm công về cơ sở dữ liệu, file control.py đọc dữ liệu trong cơ sở dữ liệu và hiển thị.

### chức năng và các hàm sử dụng note trong code, file control.py

username: techmaster, password: kubernetes2018