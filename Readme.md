# Satl
In persian bucket is Satl
In this utility you can save documents in files without any dependencies just with python

## Tutorial:
Create document

```
from satl import Satl

data = {'id': uuid4.uuid(), 'create_date': datetime.now(), 'name': 'Mohammad'}
satl = Satl(data['id'], data=data) # you can declare id by yourself
satl.save()  # save data
```

Store image
```
img = requests.get('http://yourdomain.com/image.jpg')
satl_obj.attach_file_object(img.content, 'image.jpg')
```

Count all documents
```
Satl.count()
```

Querying data
```
for satl in Satl.all():
   item = satl.load()
   print(item.pk)
   print(item['name'])
```

Check is key exists?
```
Satl.is_exists(url)
```


## API:
* update_date
* create_date
* pk
* keyword_path
* get_path
* set_keywords
* set_data
* relate_keyword
* unrelate_keyword
* rerelate_keywords
* save
* attach_file_object
* attach_file_path
* files
* count_files
* load
* get
* is_exists
* filter_by_keyword
* filter_by_date
* all
* count
