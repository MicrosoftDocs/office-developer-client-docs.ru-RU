---
<<<<<<< Название HEAD: TOCTitle свойство StayInSync (ADO): свойство StayInSync (ADO) === название: свойство StayInSync (ADO) TOCTitle: свойство StayInSync (ADO)
>>>>>>> главные ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15) ms:contentKeyID: 48542966 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="stayinsync-property-ado"></a>StayInSync Property (ADO)
=======
# <a name="stayinsync-property-ado"></a>Свойство StayInSync (ADO)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

Указывает, в объект [набора записей](recordset-object-ado.md) иерархических ли ссылку на базовый дочерние записи (то есть, *главы*) изменяется при изменении позиции строки родительского.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
=======
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
>>>>>>> master

Задает или возвращает значение **типа Boolean** . Значение по умолчанию — **True**. Если **значение True**, главы будут обновлены, если изменения объекта **набора записей** родительской строки положение; Если **значение False**, главы будет продолжать ссылаться на данные в предыдущей главе, даже если родительский объект **набора записей** изменилось положение строки.

## <a name="remarks"></a>Замечания

Это свойство применяется к иерархические наборы записей, такие как те, поддерживаемые [Службой формирования Microsoft данных для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)и должно быть равно на родительский **записей** перед дочерними извлекается **набора записей** . Это свойство упрощает переход иерархические наборы записей.

