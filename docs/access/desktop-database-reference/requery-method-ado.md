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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306715"
---
# <a name="requery-method-ado"></a><span data-ttu-id="403b9-102">Метод Requery (ADO)</span><span class="sxs-lookup"><span data-stu-id="403b9-102">Requery method (ADO)</span></span>

<span data-ttu-id="403b9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="403b9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="403b9-104">Обновляет данные в объекте [Recordset](recordset-object-ado.md) с помощью повторного выполнения запроса, на котором основан объект.</span><span class="sxs-lookup"><span data-stu-id="403b9-104">Updates the data in a [Recordset](recordset-object-ado.md) object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="403b9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="403b9-105">Syntax</span></span>

<span data-ttu-id="403b9-106">*recordset*. Параметры *requery*</span><span class="sxs-lookup"><span data-stu-id="403b9-106">*recordset*.Requery *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="403b9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="403b9-107">Parameters</span></span>

|<span data-ttu-id="403b9-108">Имя</span><span class="sxs-lookup"><span data-stu-id="403b9-108">Name</span></span> |<span data-ttu-id="403b9-109">Описание</span><span class="sxs-lookup"><span data-stu-id="403b9-109">Description</span></span>|
|:----|:----------|
|<span data-ttu-id="403b9-110">*Options*</span><span class="sxs-lookup"><span data-stu-id="403b9-110">*Options*</span></span> |<span data-ttu-id="403b9-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="403b9-111">Optional.</span></span> <span data-ttu-id="403b9-112">Битоваяmask, которая [содержит значения ExecuteOptionEnum](executeoptionenum.md) и [CommandTypeEnum,](commandtypeenum.md) влияющие на эту операцию.</span><span class="sxs-lookup"><span data-stu-id="403b9-112">A bitmask that contains [ExecuteOptionEnum](executeoptionenum.md) and [CommandTypeEnum](commandtypeenum.md) values affecting this operation.</span></span>|

> [!NOTE]
> <span data-ttu-id="403b9-113">Если *параметру Options* задан **параметр adAsyncExecute,** эта операция будет выполняться асинхронно, и после ее завершения будет выдано событие [RecordsetChangeComplete.](willchangerecordset-and-recordsetchangecomplete-events-ado.md)</span><span class="sxs-lookup"><span data-stu-id="403b9-113">If *Options* is set to **adAsyncExecute**, this operation will execute asynchronously and a [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) event will be issued when it concludes.</span></span>

<span data-ttu-id="403b9-114">Значения **ExecuteOpenEnum** **adExecuteNoRecords** или **adExecuteStream** не следует использовать с **Requery.**</span><span class="sxs-lookup"><span data-stu-id="403b9-114">The **ExecuteOpenEnum** values of **adExecuteNoRecords** or **adExecuteStream** should not be used with **Requery**.</span></span>

## <a name="remarks"></a><span data-ttu-id="403b9-115">Заметки</span><span class="sxs-lookup"><span data-stu-id="403b9-115">Remarks</span></span>

<span data-ttu-id="403b9-116">Используйте метод **Requery** для обновления всего содержимого объекта **Recordset** из источника данных путем повторной выдачи исходной команды и повторного получения данных.</span><span class="sxs-lookup"><span data-stu-id="403b9-116">Use the **Requery** method to refresh the entire contents of a **Recordset** object from the data source by reissuing the original command and retrieving the data a second time.</span></span> <span data-ttu-id="403b9-117">Вызов этого метода эквивалентен вызову методов [Close](close-method-ado.md) и [Open](open-method-ado-recordset.md) последовательно.</span><span class="sxs-lookup"><span data-stu-id="403b9-117">Calling this method is equivalent to calling the [Close](close-method-ado.md) and [Open](open-method-ado-recordset.md) methods in succession.</span></span> <span data-ttu-id="403b9-118">При редактировании текущей записи или добавлении новой записи возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="403b9-118">If you are editing the current record or adding a new record, an error occurs.</span></span>

<span data-ttu-id="403b9-119">Хотя объект **Recordset** открыт, свойства, которые определяют природу курсора ([CursorType,](cursortype-property-ado.md) [LockType,](locktype-property-ado.md) [MaxRecords](maxrecords-property-ado.md)и так далее), являются только для чтения.</span><span class="sxs-lookup"><span data-stu-id="403b9-119">While the **Recordset** object is open, the properties that define the nature of the cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), and so forth) are read-only.</span></span> <span data-ttu-id="403b9-120">Таким образом, метод **Requery** может обновить только текущий курсор.</span><span class="sxs-lookup"><span data-stu-id="403b9-120">Thus, the **Requery** method can only refresh the current cursor.</span></span> <span data-ttu-id="403b9-121">Чтобы изменить любое из свойств курсора и просмотреть результаты, необходимо использовать метод [Close,](close-method-ado.md) чтобы свойства снова стали читать и записываться.</span><span class="sxs-lookup"><span data-stu-id="403b9-121">To change any of the cursor properties and view the results, you must use the [Close](close-method-ado.md) method so that the properties become read/write again.</span></span> <span data-ttu-id="403b9-122">Затем можно изменить параметры свойства и вызвать метод [Open,](open-method-ado-recordset.md) чтобы повторно открыть курсор.</span><span class="sxs-lookup"><span data-stu-id="403b9-122">You can then change the property settings and call the [Open](open-method-ado-recordset.md) method to reopen the cursor.</span></span>

