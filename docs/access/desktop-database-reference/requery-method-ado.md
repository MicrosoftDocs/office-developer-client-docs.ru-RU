---
title: Метод reQuery (ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 249dc236d730cf773ec38fe5dd903cb64ca9b594
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306715"
---
# <a name="requery-method-ado"></a><span data-ttu-id="560f5-102">Метод reQuery (ADO)</span><span class="sxs-lookup"><span data-stu-id="560f5-102">Requery method (ADO)</span></span>

<span data-ttu-id="560f5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="560f5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="560f5-104">Обновляет данные в объекте [Recordset](recordset-object-ado.md) с помощью повторного выполнения запроса, на котором основан объект.</span><span class="sxs-lookup"><span data-stu-id="560f5-104">Updates the data in a [Recordset](recordset-object-ado.md) object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="560f5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="560f5-105">Syntax</span></span>

<span data-ttu-id="560f5-106">*набор записей*. *Параметры* запроса</span><span class="sxs-lookup"><span data-stu-id="560f5-106">*recordset*.Requery *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="560f5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="560f5-107">Parameters</span></span>

|<span data-ttu-id="560f5-108">Имя</span><span class="sxs-lookup"><span data-stu-id="560f5-108">Name</span></span> |<span data-ttu-id="560f5-109">Описание</span><span class="sxs-lookup"><span data-stu-id="560f5-109">Description</span></span>|
|:----|:----------|
|<span data-ttu-id="560f5-110">*Options*</span><span class="sxs-lookup"><span data-stu-id="560f5-110">*Options*</span></span> |<span data-ttu-id="560f5-111">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="560f5-111">Optional.</span></span> <span data-ttu-id="560f5-112">Битовая маска, содержащая значения [ексекутеоптионенум](executeoptionenum.md) и [коммандтипинум](commandtypeenum.md) , которые влияют на эту операцию.</span><span class="sxs-lookup"><span data-stu-id="560f5-112">A bitmask that contains [ExecuteOptionEnum](executeoptionenum.md) and [CommandTypeEnum](commandtypeenum.md) values affecting this operation.</span></span>|

> [!NOTE]
> <span data-ttu-id="560f5-113">Если *параметру* присвоено значение **адасинцексекуте**, эта операция выполняется асинхронно и при завершении работы будет создано событие [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="560f5-113">If *Options* is set to **adAsyncExecute**, this operation will execute asynchronously and a [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) event will be issued when it concludes.</span></span>

<span data-ttu-id="560f5-114">Значения **ексекутеопененум** для **адексекутенорекордс** или **адексекутестреам** не следует использовать вместе с параметром Requery. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="560f5-114">The **ExecuteOpenEnum** values of **adExecuteNoRecords** or **adExecuteStream** should not be used with **Requery**.</span></span>

## <a name="remarks"></a><span data-ttu-id="560f5-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="560f5-115">Remarks</span></span>

<span data-ttu-id="560f5-116">Используйте метод **reissuing** для обновления всего содержимого объекта **Recordset** из источника данных путем повторного выпуска исходной команды и извлечения данных во второй раз.</span><span class="sxs-lookup"><span data-stu-id="560f5-116">Use the **Requery** method to refresh the entire contents of a **Recordset** object from the data source by reissuing the original command and retrieving the data a second time.</span></span> <span data-ttu-id="560f5-117">Вызов этого метода эквивалентен вызову методов [Close](close-method-ado.md) и [Open](open-method-ado-recordset.md) в ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="560f5-117">Calling this method is equivalent to calling the [Close](close-method-ado.md) and [Open](open-method-ado-recordset.md) methods in succession.</span></span> <span data-ttu-id="560f5-118">При редактировании текущей записи или добавлении новой записи возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="560f5-118">If you are editing the current record or adding a new record, an error occurs.</span></span>

<span data-ttu-id="560f5-119">Пока открыт объект **Recordset** , свойства, определяющие природу курсора ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [maxRecords](maxrecords-property-ado.md)и т. д.), доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="560f5-119">While the **Recordset** object is open, the properties that define the nature of the cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), and so forth) are read-only.</span></span> <span data-ttu-id="560f5-120">Таким образом, \*\*\*\* метод Requery может обновить только текущий курсор.</span><span class="sxs-lookup"><span data-stu-id="560f5-120">Thus, the **Requery** method can only refresh the current cursor.</span></span> <span data-ttu-id="560f5-121">Чтобы изменить свойства курсора и просмотреть результаты, необходимо использовать метод [Close](close-method-ado.md) , чтобы свойства стали доступны для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="560f5-121">To change any of the cursor properties and view the results, you must use the [Close](close-method-ado.md) method so that the properties become read/write again.</span></span> <span data-ttu-id="560f5-122">Затем можно изменить параметры свойства и вызвать метод [Open](open-method-ado-recordset.md) для повторного открытия курсора.</span><span class="sxs-lookup"><span data-stu-id="560f5-122">You can then change the property settings and call the [Open](open-method-ado-recordset.md) method to reopen the cursor.</span></span>

