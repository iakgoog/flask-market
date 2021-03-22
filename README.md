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
