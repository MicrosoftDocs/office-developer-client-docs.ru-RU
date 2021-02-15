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
# <a name="cursortype-property-ado"></a><span data-ttu-id="b0d9c-102">Свойство CursorType (ADO)</span><span class="sxs-lookup"><span data-stu-id="b0d9c-102">CursorType property (ADO)</span></span>


<span data-ttu-id="b0d9c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0d9c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0d9c-104">Указывает тип курсора, используемого в [объекте Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b0d9c-104">Indicates the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b0d9c-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b0d9c-105">Settings and return values</span></span>

<span data-ttu-id="b0d9c-106">Задает или возвращает значение [CursorTypeEnum.](cursortypeenum.md)</span><span class="sxs-lookup"><span data-stu-id="b0d9c-106">Sets or returns a [CursorTypeEnum](cursortypeenum.md) value.</span></span> <span data-ttu-id="b0d9c-107">Значение по умолчанию **— adOpenForwardOnly.**</span><span class="sxs-lookup"><span data-stu-id="b0d9c-107">The default value is **adOpenForwardOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0d9c-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="b0d9c-108">Remarks</span></span>

<span data-ttu-id="b0d9c-109">Используйте свойство **CursorType,** чтобы указать тип курсора, который должен использоваться при открытии **объекта Recordset.**</span><span class="sxs-lookup"><span data-stu-id="b0d9c-109">Use the **CursorType** property to specify the type of cursor that should be used when opening the **Recordset** object.</span></span>

<span data-ttu-id="b0d9c-110">Поддерживается только **параметр adOpenStatic,** если свойство [CursorLocation](cursorlocation-property-ado.md) имеет свойство **adUseClient.**</span><span class="sxs-lookup"><span data-stu-id="b0d9c-110">Only a setting of **adOpenStatic** is supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span> <span data-ttu-id="b0d9c-111">Если установлено неподтверченные значения, ошибка не будет создана; Вместо него будет использоваться **ближайший поддерживаемый cursorType.**</span><span class="sxs-lookup"><span data-stu-id="b0d9c-111">If an unsupported value is set, then no error will result; the closest supported **CursorType** will be used instead.</span></span>

<span data-ttu-id="b0d9c-112">Если поставщик не поддерживает запрашиваемого типа курсора, он может вернуть другой тип курсора.</span><span class="sxs-lookup"><span data-stu-id="b0d9c-112">If a provider does not support the requested cursor type, it may return another cursor type.</span></span> <span data-ttu-id="b0d9c-113">Свойство **CursorType** будет изменяться в соответствие с фактическим типом курсора, который используется при открытом объекте [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b0d9c-113">The **CursorType** property will change to match the actual cursor type in use when the [Recordset](recordset-object-ado.md) object is open.</span></span> <span data-ttu-id="b0d9c-114">Чтобы проверить конкретные функции возвращенного курсора, используйте метод [Supports.](supports-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b0d9c-114">To verify specific functionality of the returned cursor, use the [Supports](supports-method-ado.md) method.</span></span> <span data-ttu-id="b0d9c-115">После закрытия объекта **Recordset** свойство **CursorType** возвращается к исходному параметру.</span><span class="sxs-lookup"><span data-stu-id="b0d9c-115">After you close the **Recordset**, the **CursorType** property reverts to its original setting.</span></span>

<span data-ttu-id="b0d9c-116">На следующей диаграмме показаны функции поставщика (которые определены константами метода **Supports),** необходимые для каждого типа курсора.</span><span class="sxs-lookup"><span data-stu-id="b0d9c-116">The following chart shows the provider functionality (identified by **Supports** method constants) required for each cursor type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0d9c-117">Для recordset этого CursorType</span><span class="sxs-lookup"><span data-stu-id="b0d9c-117">For a Recordset of this CursorType</span></span></p></th>
<th><p><span data-ttu-id="b0d9c-118">Метод Supports должен возвращать true для всех этих констант</span><span class="sxs-lookup"><span data-stu-id="b0d9c-118">The Supports method must return True for all of these constants</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0d9c-119"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="b0d9c-119"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="b0d9c-120">Нет</span><span class="sxs-lookup"><span data-stu-id="b0d9c-120">none</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0d9c-121"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="b0d9c-121"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="b0d9c-122"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="b0d9c-122"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0d9c-123"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="b0d9c-123"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="b0d9c-124"><strong>adMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="b0d9c-124"><strong>adMovePrevious</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0d9c-125"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="b0d9c-125"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="b0d9c-126"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="b0d9c-126"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="b0d9c-127">Хотя **supports\*\*\*\*(adUpdateBatch)** может иметь значение true для динамических курсоров и курсоров только вперед, для пакетных обновлений следует использовать либо набор ключей, либо статический курсор.</span><span class="sxs-lookup"><span data-stu-id="b0d9c-127">Although **Supports**(**adUpdateBatch**) may be true for dynamic and forward-only cursors, for batch updates you should use either a keyset or static cursor.</span></span> <span data-ttu-id="b0d9c-128">Установите для свойства [LockType](locktype-property-ado.md) свойство **adLockBatchOptimistic,** а для **свойства CursorLocation** — **adUseClient,** чтобы включить службу курсора для OLE DB, которая требуется для пакетных обновлений.</span><span class="sxs-lookup"><span data-stu-id="b0d9c-128">Set the [LockType](locktype-property-ado.md) property to **adLockBatchOptimistic** and the **CursorLocation** property to **adUseClient** to enable the Cursor Service for OLE DB, which is required for batch updates.</span></span>

<span data-ttu-id="b0d9c-129">Свойство **CursorType** считывалось и записывалось при закрытии объекта **Recordset** и только для чтения при его открытом режиме.</span><span class="sxs-lookup"><span data-stu-id="b0d9c-129">The **CursorType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="b0d9c-130">**Использование удаленной службы данных** При клиентском объекте Recordset свойство **CursorType** можно установить только в **adOpenStatic.**</span><span class="sxs-lookup"><span data-stu-id="b0d9c-130">**Remote Data Service Usage** When used on a client-side Recordset object, the **CursorType** property can be set only to **adOpenStatic**.</span></span>

