# mgo
使用方法
```
err:= mon.Session.DB("dev").C("template").UpdateUseAf(
        bson.M{"name":"测试模板"},
        bson.M{"$set": bson.M{"content.regs.$[reg].conf.$[con].name": "逻辑控制模式"}},
        []bson.M{
            {"reg.name": "继电器1"},
            {"con.name": "控制模式"},
        })
```
官方文档：https://docs.mongodb.com/manual/reference/command/update/
