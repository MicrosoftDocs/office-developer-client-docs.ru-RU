---
title: Свойство Index (ADO)
TOCTitle: Index property (ADO)
ms:assetid: 4cc00521-dcb4-19b2-2174-6e0e9bd42e62
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249241(v=office.15)
ms:contentKeyID: 48544715
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9f2eabf7d75ea6567ea7ca788e5a3c7451d0b75b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876983"
---
# <a name="index-property-ado"></a><span data-ttu-id="835ac-102">Свойство Index (ADO)</span><span class="sxs-lookup"><span data-stu-id="835ac-102">Index property (ADO)</span></span>


<span data-ttu-id="835ac-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="835ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="835ac-104">Указывает имя индекса в настоящее время фактически для объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="835ac-104">Indicates the name of the index currently in effect for a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="835ac-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="835ac-105">Settings and return values</span></span>

<span data-ttu-id="835ac-106">Задает или возвращает **строковое** значение, которое является именем индекса.</span><span class="sxs-lookup"><span data-stu-id="835ac-106">Sets or returns a **String** value, which is the name of the index.</span></span>

## <a name="remarks"></a><span data-ttu-id="835ac-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="835ac-107">Remarks</span></span>

<span data-ttu-id="835ac-108">Индекс с именем, свойство **Index** необходимо ранее объявленные в базовой таблице объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="835ac-108">The index named by the **Index** property must have previously been declared on the base table underlying the **Recordset** object.</span></span> <span data-ttu-id="835ac-109">То есть, индекса необходимо объявлены программными средствами как объект ADOX [индекса](index-object-adox.md) или создания базовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="835ac-109">That is, the index must have been declared programmatically either as an ADOX [Index](index-object-adox.md) object, or when the base table was created.</span></span>

<span data-ttu-id="835ac-110">Ошибка времени выполнения возникает, если индекс не может быть задано.</span><span class="sxs-lookup"><span data-stu-id="835ac-110">A run-time error will occur if the index cannot be set.</span></span> <span data-ttu-id="835ac-111">Свойство **Index** не могут задаваться:</span><span class="sxs-lookup"><span data-stu-id="835ac-111">The **Index** property cannot be set:</span></span>

  - <span data-ttu-id="835ac-112">В обработчик событий [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) или **RecordsetChangeComplete** .</span><span class="sxs-lookup"><span data-stu-id="835ac-112">Within a [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) or **RecordsetChangeComplete** event handler.</span></span>

  - <span data-ttu-id="835ac-113">Если **записей** по-прежнему выполняет операцию (который устанавливается с помощью свойства [State](state-property-ado.md) ).</span><span class="sxs-lookup"><span data-stu-id="835ac-113">If the **Recordset** is still executing an operation (which can be determined by the [State](state-property-ado.md) property).</span></span>

  - <span data-ttu-id="835ac-114">Если установлен фильтр **набора записей** с помощью свойства [фильтра](filter-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="835ac-114">If a filter has been set on the **Recordset** with the [Filter](filter-property-ado.md) property.</span></span>

<span data-ttu-id="835ac-115">Свойство **Index** можно задать успешно всегда при закрытии **набора записей** , но не будет открываться **записей** или индекс не будет использоваться, если основной поставщик поддерживает индексы.</span><span class="sxs-lookup"><span data-stu-id="835ac-115">The **Index** property can always be set successfully if the **Recordset** is closed, but the **Recordset** will not open successfully, or the index will not be usable, if the underlying provider does not support indexes.</span></span>

<span data-ttu-id="835ac-116">Если можно задать индекса, может измениться текущей позиции строки.</span><span class="sxs-lookup"><span data-stu-id="835ac-116">If the index can be set, the current row position may change.</span></span> <span data-ttu-id="835ac-117">Это приведет к обновления свойство [AbsolutePosition](absoluteposition-property-ado.md) и созданием **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md)и [MoveComplete](willmove-and-movecomplete-events-ado.md) события.</span><span class="sxs-lookup"><span data-stu-id="835ac-117">This will cause an update to the [AbsolutePosition](absoluteposition-property-ado.md) property, and the generation of **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md), and [MoveComplete](willmove-and-movecomplete-events-ado.md) events.</span></span>

<span data-ttu-id="835ac-118">Если индекс можно задать, является ли данное свойство [LockType для](locktype-property-ado.md) **adLockPessimistic** или **adLockOptimistic**неявных [UpdateBatch](updatebatch-method-ado.md) операция выполняется.</span><span class="sxs-lookup"><span data-stu-id="835ac-118">If the index can be set and the [LockType](locktype-property-ado.md) property is **adLockPessimistic** or **adLockOptimistic**, then an implicit [UpdateBatch](updatebatch-method-ado.md) operation is performed.</span></span> <span data-ttu-id="835ac-119">Это освобождает текущий и затронутых группы.</span><span class="sxs-lookup"><span data-stu-id="835ac-119">This releases the current and affected groups.</span></span> <span data-ttu-id="835ac-120">Выпущен любой существующий фильтр и текущей позиции строки изменяется в первую строку упорядоченный **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="835ac-120">Any existing filter is released, and the current row position is changed to the first row of the reordered **Recordset**.</span></span>

<span data-ttu-id="835ac-121">Свойство **Index** используется в сочетании с методом [поиска](seek-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="835ac-121">The **Index** property is used in conjunction with the [Seek](seek-method-ado.md) method.</span></span> <span data-ttu-id="835ac-122">Если базовый поставщик не поддерживает свойство **Index** и, следовательно, метод **Seek** , рекомендуется использовать метод [поиска](find-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="835ac-122">If the underlying provider does not support the **Index** property, and thus the **Seek** method, consider using the [Find](find-method-ado.md) method instead.</span></span> <span data-ttu-id="835ac-123">Определите, поддерживает ли объект **набора записей** индексов с помощью метода [поддерживает](supports-method-ado.md)**(adIndex)** .</span><span class="sxs-lookup"><span data-stu-id="835ac-123">Determine whether the **Recordset** object supports indexes with the [Supports](supports-method-ado.md)**(adIndex)** method.</span></span>

<span data-ttu-id="835ac-124">Встроенные свойства **Index** не связанные с динамическое свойство [оптимизировать](optimize-property-dynamic-ado.md) несмотря на то, что они оба работают со индексов.</span><span class="sxs-lookup"><span data-stu-id="835ac-124">The built-in **Index** property is not related to the dynamic [Optimize](optimize-property-dynamic-ado.md) property, although they both deal with indexes.</span></span>

