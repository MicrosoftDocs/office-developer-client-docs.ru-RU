---
<<<<<<< Название HEAD: TOCTitle свойство Description (ADO): Свойство Description (ADO) === название: Свойство Description (ADO) TOCTitle: Свойство Description (ADO)
>>>>>>> главные ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15) ms:contentKeyID: 48544064 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="description-property-ado"></a>Description Property (ADO)
=======
# <a name="description-property-ado"></a>Свойство Description (ADO)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

Описывает объект [Error](error-object-ado.md) .

<<<<<<< HEAD
## <a name="return-value"></a>Возвращаемое значение
=======
## <a name="return-value"></a>Возвращаемое значение
>>>>>>> master

Возвращает значение типа **String** , содержащее описание ошибки.

## <a name="remarks"></a>Замечания

Используйте свойство **Description** для получения краткое описание ошибки. Отображение этого свойства для оповещения пользователя об ошибке, не могут и не хотите обрабатывать. Строка будет получен из ADO или поставщика.

Поставщики отвечают за передачей текст определенное сообщение об ошибке в ADO. Добавляет объект [Error](error-object-ado.md) ADO коллекцию **ошибок** для каждого поставщика получает сообщение об ошибке или предупреждение его. Перечисление коллекции **ошибки** для ошибки, которые передает поставщика трассировки.

