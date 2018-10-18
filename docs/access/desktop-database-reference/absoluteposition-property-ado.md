---
<<<<<<< Название HEAD: TOCTitle свойство AbsolutePosition (ADO): ms:assetid свойство AbsolutePosition (ADO): 500be001-9fa1-177b-f19d-acf003a0cdc2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15) ms:contentKeyID: 48544787 ms.date: 09/18/2015 mtps_ версия: v=office.15
---

# <a name="absoluteposition-property-ado"></a>AbsolutePosition Property (ADO)

=== Название: свойство AbsolutePosition (ADO) TOCTitle: свойство (ADO) ms:assetid AbsolutePosition: 500be001-9fa1-177b-f19d-acf003a0cdc2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15) ms:contentKeyID: 48544787 ms.date: 10/17/2018 mtps_version: v=office.15
---

# <a name="absoluteposition-property-ado"></a>Свойство AbsolutePosition (ADO)
>>>>>>> master

**Применимо к**: Access 2013 | Office 2013

Указывает порядковый номер текущей записи объекта [набора записей](recordset-object-ado.md) .

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
=======
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
>>>>>>> master

Задает или возвращает значение типа **Long** от 1 число записей в объекте **набора записей** ([RecordCount](recordcount-property-ado.md)) либо одно из значений [PositionEnum](positionenum.md) .

## <a name="remarks"></a>Замечания

<<<<<<< HEAD в порядке для свойства **AbsolutePosition** ADO требует, используемого поставщика OLE DB реализован интерфейс IRowsetLocate.
=== Для свойства **AbsolutePosition** , ADO требует, что поставщика OLE DB, который вы используете реализовать интерфейс IRowsetLocate.
>>>>>>> master

Доступ к **AbsolutePosition** свойство **набора записей** , который был открыт для последовательного доступа или динамический курсор вызывает ошибки **adErrFeatureNotAvailable**. Другие типы курсора надлежащих позициях будут возвращены до тех пор, пока поставщик поддерживает интерфейс IRowsetScroll. Если поставщик поддерживает интерфейс *IRowsetScroll* , свойство имеет значение **adPosUnknown**. Обратитесь к документации для поставщика, чтобы определить, поддерживает ли *IRowsetScroll*.

Используйте свойство **AbsolutePosition** для переноса записей по его порядковый номер в объекте **набора записей** или для определения порядковый номер текущей записи. Поставщик должен поддерживать соответствующие функциональные возможности для этого свойства, чтобы оно было доступно.

Как и свойство [AbsolutePage](absolutepage-property-ado.md) **AbsolutePosition** на основе 1 и имеет значение 1, если текущая запись является первой записи в **набор записей**. Общее число записей в объекте **набора записей** можно получить из свойства [RecordCount](recordcount-property-ado.md) .

<<<<<<< HEAD Если свойство **AbsolutePosition** , даже в том случае, если это записи в текущей кэш-памяти, ADO перезагружает кэша с помощью новую группу записей, начиная с указанной записи. Свойство [CacheSize](cachesize-property-ado.md) определяет размер этой группы.


> [!NOTE]
> <a name="pyou-should-not-use-the-strongabsolutepositionstrong-property-as-a-surrogate-record-number-the-position-of-a-given-record-changes-when-you-delete-a-preceding-record-there-is-also-no-assurance-that-a-given-record-will-have-the-same-strongabsolutepositionstrong-if-the-strongrecordsetstrong-object-is-requeried-or-reopened-bookmarks-are-still-the-recommended-way-of-retaining-and-returning-to-a-given-position-and-are-the-only-way-of-positioning-across-all-types-of-strongrecordsetstrong-objectsp"></a><P>Не следует использовать свойство <STRONG>AbsolutePosition</STRONG> как номер заменяющего записи. Положение данной записи изменений при удалении предыдущей записи. Нет никакой гарантии, что данной записи будут иметь же <STRONG>AbsolutePosition</STRONG> , если опросить или повторном открытии в объект <STRONG>набора записей</STRONG> . Закладки будут по-прежнему рекомендуемый способ сохранения и возврата в заданной позиции и являются единственным способом размещения для всех типов объектов <STRONG>наборов записей</STRONG> .</P>
=======
Если задать свойство **AbsolutePosition** даже в том случае, если это записи в текущей кэш-памяти, ADO перезагружает кэша с новой группы записей, начиная с записью, указанной. Свойство [CacheSize](cachesize-property-ado.md) определяет размер этой группы.


> [!NOTE]
> Не следует использовать свойство **AbsolutePosition** как номер заменяющего записи. Положение данной записи изменений при удалении предыдущей записи. Нет никакой гарантии, что данной записи будут иметь же **AbsolutePosition** , если опросить или повторном открытии в объект **набора записей** . Закладки по-прежнему не рекомендуемый способ сохранения и возврата в заданной позиции, а также являются единственным способом размещения для всех типов объектов **наборов записей** .
>>>>>>> master


