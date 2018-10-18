---
<<<<<<< Название HEAD: TOCTitle свойство CursorType (ADO): свойство CursorType (ADO) === название: свойство CursorType (ADO) TOCTitle: свойство CursorType (ADO)
>>>>>>> главные ms:assetid: f42ded8f-9f92-ef03-a198-ffb892324611 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250239(v=office.15) ms:contentKeyID: 48548682 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="cursortype-property-ado"></a>CursorType Property (ADO)
=======
# <a name="cursortype-property-ado"></a>Свойство CursorType (ADO)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

Указывает тип курсора, используемого в объекте [набора записей](recordset-object-ado.md) .

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
=======
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
>>>>>>> master

Задает или возвращает значение [CursorTypeEnum](cursortypeenum.md) . Значение по умолчанию — **adOpenForwardOnly**.

## <a name="remarks"></a>Замечания

Свойство **CursorType** определяет тип указателя, который должен использоваться при открытии объекта **набора записей** .

Только параметр **adOpenStatic** поддерживается, если свойство [CursorLocation](cursorlocation-property-ado.md) имеет значение **adUseClient**. Если задано значение не поддерживается, сообщение об ошибке не приведет к; ближайший поддерживаемый **CursorType** будет использоваться.

Если поставщик поддерживает курсором запрошенного типа, он может вернуть курсор другого типа. Свойство **CursorType** изменится в соответствии в используемый тип фактический курсора при открытом объекта [набора записей](recordset-object-ado.md) . Проверка определенных функций возвращенные курсора, используйте метод [поддерживает](supports-method-ado.md) . После закрытия **набора записей**свойство **CursorType** возвращается в исходное значение.

В приведенной ниже диаграмме показано функциональности поставщика (обозначенный **поддерживает** метод константы) требуется для каждого типа курсора.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Для набора записей в этом CursorType</p></th>
<th><p>Поддерживает метод должен возвращать значение True для всех этих констант</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p><strong>adMovePrevious</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>Несмотря на то, что <STRONG>поддерживает</STRONG>(<STRONG>adUpdateBatch</STRONG>) может иметь значение true для динамического и однонаправленные курсоры, для пакетного обновления следует использовать статический курсор или набора ключей. Присвойте свойству <A href="locktype-property-ado.md">LockType для</A> <STRONG>adLockBatchOptimistic</STRONG> и <STRONG>CursorLocation</STRONG> свойства <STRONG>adUseClient</STRONG> , чтобы включить службу курсора для OLE DB, который необходим для пакетного обновления.</P>



Свойство **CursorType** при чтение и запись **набора записей** закрытой и только для чтения, при открытии.

**Службы удаленных данных об использовании** При использовании в объект набора записей со стороны клиента, свойство **CursorType** можно задать только к **adOpenStatic**.

