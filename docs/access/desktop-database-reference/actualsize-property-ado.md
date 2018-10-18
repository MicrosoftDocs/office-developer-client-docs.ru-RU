---
<<<<<<< Название HEAD: TOCTitle свойство ActualSize (ADO): ms:assetid свойство ActualSize (ADO): 020a414d-e6aa-5fb9-9b77-bd9d10124f8a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15) ms:contentKeyID: 48542949 ms.date: 09/18/2015 mtps_version: v = Office.15
---

# <a name="actualsize-property-ado"></a>ActualSize Property (ADO)
=== Название: свойство ActualSize (ADO) TOCTitle: свойство (ADO) ms:assetid ActualSize: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15) ms:contentKeyID: 48542949 ms.date: 10/16/2018 mtps_version: v=office.15
---

# <a name="actualsize-property-ado"></a>Свойство ActualSize (ADO)
>>>>>>> master

**Применимо к**: Access 2013 | Office 2013

Фактическая длина значения поля.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
=======
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
>>>>>>> master

Возвращает значение типа **Long** . Некоторые поставщики могут разрешить это свойство должно быть задано для резервирования пространства для данных больших двоичных ОБЪЕКТОВ, в котором case значение по умолчанию равно 0.

## <a name="remarks"></a>Замечания

Свойство **ActualSize** возвращает фактический длины значения объекта [поля](field-object-ado.md) . Для всех полей **ActualSize** свойство доступно только для чтения. Если ADO не может быть определен значение **поля** объекта, свойство **ActualSize** возвращает **adUnknown**.

<<<<<<< HEAD **ActualSize** и [DefinedSize](definedsize-property-ado.md) свойства отличаются, как показано в следующем примере. Объект **Field** с типом объявленные **adVarChar** и максимальную длину 50 символов возвращает значение свойства **DefinedSize** 50, но она возвращает значение свойства **ActualSize** — это длина данных, сохраненных в процессе работы Текущая запись. **Поля** с **DefinedSize** быстрее, чем 255 байт обрабатывается как столбцы переменной длины.
=== Свойства **ActualSize** и [DefinedSize](definedsize-property-ado.md) не совпадают. Объект **Field** с типом объявленные **adVarChar** и максимальную длину 50 символов возвращает значение свойства **DefinedSize** 50, но она возвращает значение свойства **ActualSize** — это длина данных, сохраненных в процессе работы Текущая запись. **Поля** с **DefinedSize** быстрее, чем 255 байт обрабатывается как столбцы переменной длины.
>>>>>>> master

