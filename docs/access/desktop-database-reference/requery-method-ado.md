---
title: Метод Requery (ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 249dc236d730cf773ec38fe5dd903cb64ca9b594
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705682"
---
# <a name="requery-method-ado"></a><span data-ttu-id="18139-102">Метод Requery (ADO)</span><span class="sxs-lookup"><span data-stu-id="18139-102">Requery method (ADO)</span></span>

<span data-ttu-id="18139-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18139-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18139-104">Обновляет данные в объект [набора записей](recordset-object-ado.md) , повторное выполнение запросов, на котором основан объект.</span><span class="sxs-lookup"><span data-stu-id="18139-104">Updates the data in a [Recordset](recordset-object-ado.md) object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="18139-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18139-105">Syntax</span></span>

<span data-ttu-id="18139-106">*набор записей*. Обновление *параметров*</span><span class="sxs-lookup"><span data-stu-id="18139-106">*recordset*.Requery *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="18139-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="18139-107">Parameters</span></span>

|<span data-ttu-id="18139-108">Имя</span><span class="sxs-lookup"><span data-stu-id="18139-108">Name</span></span> |<span data-ttu-id="18139-109">Описание</span><span class="sxs-lookup"><span data-stu-id="18139-109">Description</span></span>|
|:----|:----------|
|<span data-ttu-id="18139-110">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="18139-110">*Options*</span></span> |<span data-ttu-id="18139-111">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="18139-111">Optional.</span></span> <span data-ttu-id="18139-112">Битовая маска, которая содержит значения [ExecuteOptionEnum](executeoptionenum.md) и [CommandTypeEnum](commandtypeenum.md) влияния на этой операции.</span><span class="sxs-lookup"><span data-stu-id="18139-112">A bitmask that contains [ExecuteOptionEnum](executeoptionenum.md) and [CommandTypeEnum](commandtypeenum.md) values affecting this operation.</span></span>|

> [!NOTE]
> <span data-ttu-id="18139-113">Если *Параметры* **adAsyncExecute**, эта операция выполняется асинхронно и события [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) будет выдается, когда она завершается.</span><span class="sxs-lookup"><span data-stu-id="18139-113">If *Options* is set to **adAsyncExecute**, this operation will execute asynchronously and a [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) event will be issued when it concludes.</span></span>

<span data-ttu-id="18139-114">Значения **ExecuteOpenEnum** **adExecuteNoRecords** или **adExecuteStream** не должен использоваться с **повторный запрос**.</span><span class="sxs-lookup"><span data-stu-id="18139-114">The **ExecuteOpenEnum** values of **adExecuteNoRecords** or **adExecuteStream** should not be used with **Requery**.</span></span>

## <a name="remarks"></a><span data-ttu-id="18139-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="18139-115">Remarks</span></span>

<span data-ttu-id="18139-116">Используйте метод **повторный запрос** для обновления все содержимое объекта **набора записей** из источника данных путем получения исходного команды и извлечение данных еще раз.</span><span class="sxs-lookup"><span data-stu-id="18139-116">Use the **Requery** method to refresh the entire contents of a **Recordset** object from the data source by reissuing the original command and retrieving the data a second time.</span></span> <span data-ttu-id="18139-117">Вызов данного метода эквивалентен вызову метода [Close](close-method-ado.md) и [открытия](open-method-ado-recordset.md) последовательно.</span><span class="sxs-lookup"><span data-stu-id="18139-117">Calling this method is equivalent to calling the [Close](close-method-ado.md) and [Open](open-method-ado-recordset.md) methods in succession.</span></span> <span data-ttu-id="18139-118">Если вы изменяете текущей записи или добавлять новую запись, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="18139-118">If you are editing the current record or adding a new record, an error occurs.</span></span>

<span data-ttu-id="18139-119">Когда открыт объекта **набора записей** , свойства, которые определяют характер курсор ([CursorType](cursortype-property-ado.md), [LockType для](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md)и т. д.) доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="18139-119">While the **Recordset** object is open, the properties that define the nature of the cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), and so forth) are read-only.</span></span> <span data-ttu-id="18139-120">Таким образом метод **повторный запрос** можно только обновить курсора.</span><span class="sxs-lookup"><span data-stu-id="18139-120">Thus, the **Requery** method can only refresh the current cursor.</span></span> <span data-ttu-id="18139-121">Чтобы изменить свойства курсора и просмотреть результаты, необходимо использовать метод [Close](close-method-ado.md) , чтобы свойства становятся чтение и запись еще раз.</span><span class="sxs-lookup"><span data-stu-id="18139-121">To change any of the cursor properties and view the results, you must use the [Close](close-method-ado.md) method so that the properties become read/write again.</span></span> <span data-ttu-id="18139-122">Затем можно изменить значения свойств и вызвать метод [Open](open-method-ado-recordset.md) , чтобы снова открыть курсор.</span><span class="sxs-lookup"><span data-stu-id="18139-122">You can then change the property settings and call the [Open](open-method-ado-recordset.md) method to reopen the cursor.</span></span>

