---
title: Свойство Index (ADO)
TOCTitle: Index property (ADO)
ms:assetid: 4cc00521-dcb4-19b2-2174-6e0e9bd42e62
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249241(v=office.15)
ms:contentKeyID: 48544715
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d436ec9102c4c75688b6c6ac973ca85e8c280d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291708"
---
# <a name="index-property-ado"></a><span data-ttu-id="4dcdc-102">Свойство Index (ADO)</span><span class="sxs-lookup"><span data-stu-id="4dcdc-102">Index property (ADO)</span></span>


<span data-ttu-id="4dcdc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4dcdc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4dcdc-104">Указывает имя индекса, который в настоящее время действует для [объекта Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4dcdc-104">Indicates the name of the index currently in effect for a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4dcdc-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="4dcdc-105">Settings and return values</span></span>

<span data-ttu-id="4dcdc-106">Задает или возвращает **значение String,** которое является именем индекса.</span><span class="sxs-lookup"><span data-stu-id="4dcdc-106">Sets or returns a **String** value, which is the name of the index.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dcdc-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="4dcdc-107">Remarks</span></span>

<span data-ttu-id="4dcdc-108">Индекс, названный **свойством Index,** должен быть объявлен ранее в базовой таблице, в основе которого находится объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="4dcdc-108">The index named by the **Index** property must have previously been declared on the base table underlying the **Recordset** object.</span></span> <span data-ttu-id="4dcdc-109">То есть индекс должен быть объявлен программным путем либо [](index-object-adox.md) как объект индекса ADOX, либо при создания базовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="4dcdc-109">That is, the index must have been declared programmatically either as an ADOX [Index](index-object-adox.md) object, or when the base table was created.</span></span>

<span data-ttu-id="4dcdc-110">Ошибка при запуске произойдет, если не удается установить индекс.</span><span class="sxs-lookup"><span data-stu-id="4dcdc-110">A run-time error will occur if the index cannot be set.</span></span> <span data-ttu-id="4dcdc-111">Свойство **Index** не может быть установлено:</span><span class="sxs-lookup"><span data-stu-id="4dcdc-111">The **Index** property cannot be set:</span></span>

  - <span data-ttu-id="4dcdc-112">В [обработнике событий WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) или **RecordsetChangeComplete.**</span><span class="sxs-lookup"><span data-stu-id="4dcdc-112">Within a [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) or **RecordsetChangeComplete** event handler.</span></span>

  - <span data-ttu-id="4dcdc-113">Если **в Recordset** по-прежнему выполняется операция (которая может быть определена государственным [свойством).](state-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4dcdc-113">If the **Recordset** is still executing an operation (which can be determined by the [State](state-property-ado.md) property).</span></span>

  - <span data-ttu-id="4dcdc-114">Если в наборе **Recordset** установлен фильтр с [свойством Filter.](filter-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4dcdc-114">If a filter has been set on the **Recordset** with the [Filter](filter-property-ado.md) property.</span></span>

<span data-ttu-id="4dcdc-115">Свойство **Index** всегда можно успешно зафиксировать, если набор **recordset** закрыт, но **recordset** не откроется успешно, или индекс не будет использовать, если поставщик не поддерживает индексы.</span><span class="sxs-lookup"><span data-stu-id="4dcdc-115">The **Index** property can always be set successfully if the **Recordset** is closed, but the **Recordset** will not open successfully, or the index will not be usable, if the underlying provider does not support indexes.</span></span>

<span data-ttu-id="4dcdc-116">Если можно установить индекс, текущая позиция строки может измениться.</span><span class="sxs-lookup"><span data-stu-id="4dcdc-116">If the index can be set, the current row position may change.</span></span> <span data-ttu-id="4dcdc-117">Это приведет к обновлению свойства [AbsolutePosition](absoluteposition-property-ado.md) и поколению **событий WillChangeRecordset,** **RecordsetChangeComplete,** WillMove и [MoveComplete.](willmove-and-movecomplete-events-ado.md) [](willmove-and-movecomplete-events-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4dcdc-117">This will cause an update to the [AbsolutePosition](absoluteposition-property-ado.md) property, and the generation of **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md), and [MoveComplete](willmove-and-movecomplete-events-ado.md) events.</span></span>

<span data-ttu-id="4dcdc-118">Если можно установить индекс и свойство [LockType](locktype-property-ado.md) является **adLockPessimistic** или **adLockOptimistic,** то выполняется неявная операция [UpdateBatch.](updatebatch-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4dcdc-118">If the index can be set and the [LockType](locktype-property-ado.md) property is **adLockPessimistic** or **adLockOptimistic**, then an implicit [UpdateBatch](updatebatch-method-ado.md) operation is performed.</span></span> <span data-ttu-id="4dcdc-119">Это освобождает текущие и затронутые группы.</span><span class="sxs-lookup"><span data-stu-id="4dcdc-119">This releases the current and affected groups.</span></span> <span data-ttu-id="4dcdc-120">Любой существующий фильтр освобожден, а текущая позиция строки изменена на первую строку переустановленного **Набор записей.**</span><span class="sxs-lookup"><span data-stu-id="4dcdc-120">Any existing filter is released, and the current row position is changed to the first row of the reordered **Recordset**.</span></span>

<span data-ttu-id="4dcdc-121">Свойство **Index** используется совместно с методом [Seek.](seek-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4dcdc-121">The **Index** property is used in conjunction with the [Seek](seek-method-ado.md) method.</span></span> <span data-ttu-id="4dcdc-122">Если поставщик не поддерживает свойство **Index** и, следовательно, метод **Seek,** подумайте об использовании метода [Find.](find-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4dcdc-122">If the underlying provider does not support the **Index** property, and thus the **Seek** method, consider using the [Find](find-method-ado.md) method instead.</span></span> <span data-ttu-id="4dcdc-123">Определите, поддерживает ли объект **Recordset** индексы методом [Supports](supports-method-ado.md)**(adIndex).**</span><span class="sxs-lookup"><span data-stu-id="4dcdc-123">Determine whether the **Recordset** object supports indexes with the [Supports](supports-method-ado.md)**(adIndex)** method.</span></span>

<span data-ttu-id="4dcdc-124">Встроенное свойство **Index** не связано с динамическим свойством Оптимизируйте, хотя оба они касаются индексов. [](optimize-property-dynamic-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4dcdc-124">The built-in **Index** property is not related to the dynamic [Optimize](optimize-property-dynamic-ado.md) property, although they both deal with indexes.</span></span>

