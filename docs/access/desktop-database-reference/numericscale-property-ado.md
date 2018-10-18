---
<<<<<<< Название HEAD: TOCTitle свойство NumericScale (ADO): свойство NumericScale (ADO) === название: свойство NumericScale (ADO) TOCTitle: свойство NumericScale (ADO)
>>>>>>> главные ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15) ms:contentKeyID: 48544824 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="numericscale-property-ado"></a>NumericScale Property (ADO)
=======
# <a name="numericscale-property-ado"></a>Свойство NumericScale (ADO)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

Указывает масштаб числовых значений в объекте [параметра](parameter-object-ado.md) или [поля](field-object-ado.md) .

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
=======
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
>>>>>>> master

Задает или возвращает **битное** значение, указывающее количество десятичных разрядов, к которым будут разрешены числовых значений.

## <a name="remarks"></a>Замечания

Свойство **NumericScale** определяет количество цифр справа от десятичной запятой будет использоваться для представления значений для числовых объекта **параметра** или **поля** .

Для **параметра** объектов свойство **NumericScale** — чтение и запись.

Для объекта **поля** **NumericScale** обычно доступны только для чтения. Тем не менее для новых объектов **полей** , к коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md), **NumericScale** — чтение и запись только после указано [значение](value-property-ado.md) свойства для **поля** и поставщика данных успешно добавил новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **полей** .

