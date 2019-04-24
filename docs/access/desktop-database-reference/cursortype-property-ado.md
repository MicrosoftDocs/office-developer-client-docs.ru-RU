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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295186"
---
# <a name="cursortype-property-ado"></a><span data-ttu-id="c5a9c-102">Свойство CursorType (ADO)</span><span class="sxs-lookup"><span data-stu-id="c5a9c-102">CursorType property (ADO)</span></span>


<span data-ttu-id="c5a9c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5a9c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5a9c-104">Указывает тип курсора, используемого в объекте [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c5a9c-104">Indicates the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="c5a9c-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c5a9c-105">Settings and return values</span></span>

<span data-ttu-id="c5a9c-106">Задает или возвращает значение [курсортипинум](cursortypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="c5a9c-106">Sets or returns a [CursorTypeEnum](cursortypeenum.md) value.</span></span> <span data-ttu-id="c5a9c-107">Значение по умолчанию — **адопенфорвардонли**.</span><span class="sxs-lookup"><span data-stu-id="c5a9c-107">The default value is **adOpenForwardOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5a9c-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="c5a9c-108">Remarks</span></span>

<span data-ttu-id="c5a9c-109">Используйте свойство **CursorType** , чтобы указать тип курсора, который следует использовать при открытии объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c5a9c-109">Use the **CursorType** property to specify the type of cursor that should be used when opening the **Recordset** object.</span></span>

<span data-ttu-id="c5a9c-110">Если свойству [CursorLocation](cursorlocation-property-ado.md) присвоено значение **Адусеклиент**, поддерживается только параметр **адопенстатик** .</span><span class="sxs-lookup"><span data-stu-id="c5a9c-110">Only a setting of **adOpenStatic** is supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span> <span data-ttu-id="c5a9c-111">Если задано неподдерживаемое значение, ошибка не будет возникать; Вместо этого будет использоваться ближайшее поддерживаемое **CursorType** .</span><span class="sxs-lookup"><span data-stu-id="c5a9c-111">If an unsupported value is set, then no error will result; the closest supported **CursorType** will be used instead.</span></span>

<span data-ttu-id="c5a9c-112">Если поставщик не поддерживает запрошенный тип курсора, он может вернуть другой тип курсора.</span><span class="sxs-lookup"><span data-stu-id="c5a9c-112">If a provider does not support the requested cursor type, it may return another cursor type.</span></span> <span data-ttu-id="c5a9c-113">Свойство **CursorType** будет изменено для согласования с фактическим типом курсора, используемым при открытии объекта [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c5a9c-113">The **CursorType** property will change to match the actual cursor type in use when the [Recordset](recordset-object-ado.md) object is open.</span></span> <span data-ttu-id="c5a9c-114">Чтобы проверить определенные функциональные возможности возвращаемого курсора, используйте [](supports-method-ado.md) метод Supports.</span><span class="sxs-lookup"><span data-stu-id="c5a9c-114">To verify specific functionality of the returned cursor, use the [Supports](supports-method-ado.md) method.</span></span> <span data-ttu-id="c5a9c-115">После закрытия **набора записей**свойство **CursorType** возвращается к исходному значению.</span><span class="sxs-lookup"><span data-stu-id="c5a9c-115">After you close the **Recordset**, the **CursorType** property reverts to its original setting.</span></span>

<span data-ttu-id="c5a9c-116">На следующей диаграмме показаны функциональные возможности поставщика (определяемые с помощью констант методов), необходимые для каждого типа курсора. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c5a9c-116">The following chart shows the provider functionality (identified by **Supports** method constants) required for each cursor type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5a9c-117">Для набора записей этого CursorType</span><span class="sxs-lookup"><span data-stu-id="c5a9c-117">For a Recordset of this CursorType</span></span></p></th>
<th><p><span data-ttu-id="c5a9c-118">Метод Supports должен возвращать значение true для всех этих констант</span><span class="sxs-lookup"><span data-stu-id="c5a9c-118">The Supports method must return True for all of these constants</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5a9c-119"><strong>Адопенфорвардонли</strong></span><span class="sxs-lookup"><span data-stu-id="c5a9c-119"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a9c-120">нет</span><span class="sxs-lookup"><span data-stu-id="c5a9c-120">none</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a9c-121"><strong>Адопенкэйсет</strong></span><span class="sxs-lookup"><span data-stu-id="c5a9c-121"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a9c-122"><strong>адбукмарк</strong>, <strong>адхолдрекордс</strong>, <strong>адмовепревиаус</strong>, <strong>адресинк</strong></span><span class="sxs-lookup"><span data-stu-id="c5a9c-122"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a9c-123"><strong>Адопендинамик</strong></span><span class="sxs-lookup"><span data-stu-id="c5a9c-123"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a9c-124"><strong>Адмовепревиаус</strong></span><span class="sxs-lookup"><span data-stu-id="c5a9c-124"><strong>adMovePrevious</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a9c-125"><strong>Адопенстатик</strong></span><span class="sxs-lookup"><span data-stu-id="c5a9c-125"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a9c-126"><strong>адбукмарк</strong>, <strong>адхолдрекордс</strong>, <strong>адмовепревиаус</strong>, <strong>адресинк</strong></span><span class="sxs-lookup"><span data-stu-id="c5a9c-126"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="c5a9c-127">Несмотря на то, что **поддерживается**(**адупдатебатч**) для динамических однонаправленных курсоров и однонаправленных курсоров, для пакетных обновлений необходимо использовать указатель KEYSET или статический.</span><span class="sxs-lookup"><span data-stu-id="c5a9c-127">Although **Supports**(**adUpdateBatch**) may be true for dynamic and forward-only cursors, for batch updates you should use either a keyset or static cursor.</span></span> <span data-ttu-id="c5a9c-128">ПриСвойте свойству [LockType](locktype-property-ado.md) значение **адлоккбатчоптимистик** , а свойству **CursorLocation** — значение **адусеклиент** , чтобы включить службу курсора для OLE DB, которая необходима для пакетных обновлений.</span><span class="sxs-lookup"><span data-stu-id="c5a9c-128">Set the [LockType](locktype-property-ado.md) property to **adLockBatchOptimistic** and the **CursorLocation** property to **adUseClient** to enable the Cursor Service for OLE DB, which is required for batch updates.</span></span>

<span data-ttu-id="c5a9c-129">Свойство **CursorType** доступно для чтения и записи, когда **набор записей** закрывается и только для чтения, когда он открыт.</span><span class="sxs-lookup"><span data-stu-id="c5a9c-129">The **CursorType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="c5a9c-130">**Использование удаленной службы данных** При использовании в объекте Recordset на стороне клиента свойство **CursorType** можно задать только для **адопенстатик**.</span><span class="sxs-lookup"><span data-stu-id="c5a9c-130">**Remote Data Service Usage**When used on a client-side Recordset object, the **CursorType** property can be set only to **adOpenStatic**.</span></span>

