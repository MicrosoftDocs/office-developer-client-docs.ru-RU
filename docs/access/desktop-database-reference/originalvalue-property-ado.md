---
<<<<<<< Название HEAD: TOCTitle свойство OriginalValue (ADO): свойство OriginalValue (ADO) === название: свойство OriginalValue (ADO) TOCTitle: свойство OriginalValue (ADO)
>>>>>>> главные ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15) ms:contentKeyID: 48542974 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="originalvalue-property-ado"></a>OriginalValue Property (ADO)
=======
# <a name="originalvalue-property-ado"></a>Свойство OriginalValue (ADO)
>>>>>>> master

**Применимо к**: Access 2013 | Office 2013

Указывает значение [поля](field-object-ado.md) , которое существовало в записи до внесения изменений.

<<<<<<< HEAD
## <a name="return-value"></a>Возвращаемое значение
=======
## <a name="return-value"></a>Возвращаемое значение
>>>>>>> master

Возвращает значение **типа Variant** , который представляет значение поля до изменения.

## <a name="remarks"></a>Замечания

Свойство **OriginalValue** возвращает исходное значение поля для поля из текущей записи.

В *режиме немедленное обновление* (где поставщик записывает изменения к базовому источнику данных после вызова метода [обновления](update-method-ado.md) ) это свойство **OriginalValue** возвращает значение поля, существовавшего до внесения изменений (то есть, поскольку Последнее **обновление** вызова метода). Это то же значение, метод [CancelUpdate](cancelupdate-method-ado.md) используется для замены свойства [Value](value-property-ado.md) .

В *пакетном режиме обновления* (в котором поставщик кэширует несколько изменений и записывает их в источнике данных только при вызове метода [UpdateBatch](updatebatch-method-ado.md) ) это свойство **OriginalValue** возвращает значение поля, существовавшего до какие-либо изменяет (то есть, с момента последнего метода **UpdateBatch** звонков). Это то же значение, метод [CancelBatch](cancelbatch-method-ado.md) используется для замены свойства **Value** . При использовании этого свойства с помощью свойства [UnderlyingValue](underlyingvalue-property-ado.md) можно разрешения конфликтов с помощью пакета обновления.

## <a name="record"></a>Запись

Для [записи](record-object-ado.md) объектов **OriginalValue** свойство будет пустым для полей, добавлены, прежде чем будет вызван метод [Update](update-method-ado.md) .

