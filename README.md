# Learn Flask

```
export FLASK_APP=market.py

export FLASK_DEBUG=1

flask run
```

```
pip install flask-sqlalchemy

python

from market import db
db.create_all()
from market import Item
item1 = Item(name='iPhone 10', price=500, barcode='854796214565', description='desc')
db.session.add(item1)
db.session.commit()
Item.query.all()

for item in Item.query.filter_by(price=500):
	item.name
```
`sqlitebrower.org`

```
P7
python⏎
from market.models import db
db.drop_all()
db.create_all()
from market.models import User, Item
u1 = User(username='jsc', password_hash='123456', email_address='jsc@jsc.com')
db.session.add(u1)
db.session.commit()
User.query.all()
i1 = Item(name='IPhone 10', description='description', barcode='123456789', price=800)
db.session.add(i1)
db.session.commit()
i2 = Item(name='Laptop', description='description2', barcode='6543215654', price=1000)
db.session.add(i2)
db.session.commit()
Item.query.all()
item1 = Item.query.filter_by(name='Iphone 10')
item1⏎
item1 = Item.query.filter_by(name='Iphone 10').first()
item1⏎
item1 = Item.query.filter_by(name='Iphone 10').first()
item1.owner = User.query.filter_by(username='jsc').first()
db.session.add(item1)
db.session.commit()
```
