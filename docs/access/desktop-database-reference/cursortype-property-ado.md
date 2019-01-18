---
title: Свойство CursorType (ADO)
TOCTitle: CursorType property (ADO)
ms:assetid: f42ded8f-9f92-ef03-a198-ffb892324611
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250239(v=office.15)
ms:contentKeyID: 48548682
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7cdb32bb8ff9bb6e0556a87de0efe82cd919dbe2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700761"
---
# <a name="cursortype-property-ado"></a><span data-ttu-id="bf646-102">Свойство CursorType (ADO)</span><span class="sxs-lookup"><span data-stu-id="bf646-102">CursorType property (ADO)</span></span>


<span data-ttu-id="bf646-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf646-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bf646-104">Указывает тип курсора, используемого в объекте [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bf646-104">Indicates the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="bf646-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="bf646-105">Settings and return values</span></span>

<span data-ttu-id="bf646-106">Задает или возвращает значение [CursorTypeEnum](cursortypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="bf646-106">Sets or returns a [CursorTypeEnum](cursortypeenum.md) value.</span></span> <span data-ttu-id="bf646-107">Значение по умолчанию — **adOpenForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="bf646-107">The default value is **adOpenForwardOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf646-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="bf646-108">Remarks</span></span>

<span data-ttu-id="bf646-109">Свойство **CursorType** определяет тип указателя, который должен использоваться при открытии объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="bf646-109">Use the **CursorType** property to specify the type of cursor that should be used when opening the **Recordset** object.</span></span>

<span data-ttu-id="bf646-110">Только параметр **adOpenStatic** поддерживается, если свойство [CursorLocation](cursorlocation-property-ado.md) имеет значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="bf646-110">Only a setting of **adOpenStatic** is supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span> <span data-ttu-id="bf646-111">Если задано значение не поддерживается, сообщение об ошибке не приведет к; ближайший поддерживаемый **CursorType** будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="bf646-111">If an unsupported value is set, then no error will result; the closest supported **CursorType** will be used instead.</span></span>

<span data-ttu-id="bf646-112">Если поставщик поддерживает курсором запрошенного типа, он может вернуть курсор другого типа.</span><span class="sxs-lookup"><span data-stu-id="bf646-112">If a provider does not support the requested cursor type, it may return another cursor type.</span></span> <span data-ttu-id="bf646-113">Свойство **CursorType** изменится в соответствии в используемый тип фактический курсора при открытом объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bf646-113">The **CursorType** property will change to match the actual cursor type in use when the [Recordset](recordset-object-ado.md) object is open.</span></span> <span data-ttu-id="bf646-114">Проверка определенных функций возвращенные курсора, используйте метод [поддерживает](supports-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bf646-114">To verify specific functionality of the returned cursor, use the [Supports](supports-method-ado.md) method.</span></span> <span data-ttu-id="bf646-115">После закрытия **набора записей**свойство **CursorType** возвращается в исходное значение.</span><span class="sxs-lookup"><span data-stu-id="bf646-115">After you close the **Recordset**, the **CursorType** property reverts to its original setting.</span></span>

<span data-ttu-id="bf646-116">В приведенной ниже диаграмме показано функциональности поставщика (обозначенный **поддерживает** метод константы) требуется для каждого типа курсора.</span><span class="sxs-lookup"><span data-stu-id="bf646-116">The following chart shows the provider functionality (identified by **Supports** method constants) required for each cursor type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf646-117">Для набора записей в этом CursorType</span><span class="sxs-lookup"><span data-stu-id="bf646-117">For a Recordset of this CursorType</span></span></p></th>
<th><p><span data-ttu-id="bf646-118">Поддерживает метод должен возвращать значение True для всех этих констант</span><span class="sxs-lookup"><span data-stu-id="bf646-118">The Supports method must return True for all of these constants</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf646-119"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="bf646-119"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="bf646-120">none</span><span class="sxs-lookup"><span data-stu-id="bf646-120">none</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf646-121"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="bf646-121"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="bf646-122"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="bf646-122"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf646-123"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="bf646-123"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="bf646-124"><strong>adMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="bf646-124"><strong>adMovePrevious</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf646-125"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="bf646-125"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="bf646-126"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="bf646-126"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="bf646-127">Несмотря на то, что **поддерживает**(**adUpdateBatch**) может иметь значение true для динамического и однонаправленные курсоры, для пакетного обновления следует использовать статический курсор или набора ключей.</span><span class="sxs-lookup"><span data-stu-id="bf646-127">Although **Supports**(**adUpdateBatch**) may be true for dynamic and forward-only cursors, for batch updates you should use either a keyset or static cursor.</span></span> <span data-ttu-id="bf646-128">Присвойте свойству [LockType для](locktype-property-ado.md) **adLockBatchOptimistic** и **CursorLocation** свойства **adUseClient** , чтобы включить службу курсора для OLE DB, который необходим для пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="bf646-128">Set the [LockType](locktype-property-ado.md) property to **adLockBatchOptimistic** and the **CursorLocation** property to **adUseClient** to enable the Cursor Service for OLE DB, which is required for batch updates.</span></span>

<span data-ttu-id="bf646-129">Свойство **CursorType** при чтение и запись **набора записей** закрытой и только для чтения, при открытии.</span><span class="sxs-lookup"><span data-stu-id="bf646-129">The **CursorType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="bf646-130">**Службы удаленных данных об использовании** При использовании в объект набора записей со стороны клиента, свойство **CursorType** можно задать только к **adOpenStatic**.</span><span class="sxs-lookup"><span data-stu-id="bf646-130">**Remote Data Service Usage**When used on a client-side Recordset object, the **CursorType** property can be set only to **adOpenStatic**.</span></span>

