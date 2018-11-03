---
title: Метод Requery (ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 588f99d495716ca3c40376ce323d7c1557da9319
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925802"
---
# <a name="requery-method-ado"></a><span data-ttu-id="e3c9b-102">Метод Requery (ADO)</span><span class="sxs-lookup"><span data-stu-id="e3c9b-102">Requery method (ADO)</span></span>


<span data-ttu-id="e3c9b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3c9b-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="e3c9b-104">Обновляет данные в объект [набора записей](recordset-object-ado.md) , повторное выполнение запросов, на котором основан объект.</span><span class="sxs-lookup"><span data-stu-id="e3c9b-104">Updates the data in a [Recordset](recordset-object-ado.md) object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3c9b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3c9b-105">Syntax</span></span>

<span data-ttu-id="e3c9b-106">*набор записей*. Обновление *параметров*</span><span class="sxs-lookup"><span data-stu-id="e3c9b-106">*recordset*.Requery *Options*</span></span>

## <a name="parameter"></a><span data-ttu-id="e3c9b-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="e3c9b-107">Parameter</span></span>

  - <span data-ttu-id="e3c9b-108">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="e3c9b-108">*Options*</span></span>

  - <span data-ttu-id="e3c9b-109">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="e3c9b-109">Optional.</span></span> <span data-ttu-id="e3c9b-110">Битовая маска, которая содержит значения [ExecuteOptionEnum](executeoptionenum.md) и [CommandTypeEnum](commandtypeenum.md) влияния на этой операции.</span><span class="sxs-lookup"><span data-stu-id="e3c9b-110">A bitmask that contains [ExecuteOptionEnum](executeoptionenum.md) and [CommandTypeEnum](commandtypeenum.md) values affecting this operation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e3c9b-111">Если <EM>Параметры</EM> <STRONG>adAsyncExecute</STRONG>, эта операция выполняется асинхронно и события <A href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</A> будет выдается, когда она завершается.</span><span class="sxs-lookup"><span data-stu-id="e3c9b-111">If <EM>Options</EM> is set to <STRONG>adAsyncExecute</STRONG>, this operation will execute asynchronously and a <A href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</A> event will be issued when it concludes.</span></span></P>



<span data-ttu-id="e3c9b-112">Значения **ExecuteOpenEnum** **adExecuteNoRecords** или **adExecuteStream** не должен использоваться с **повторный запрос**.</span><span class="sxs-lookup"><span data-stu-id="e3c9b-112">The **ExecuteOpenEnum** values of **adExecuteNoRecords** or **adExecuteStream** should not be used with **Requery**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3c9b-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="e3c9b-113">Remarks</span></span>

<span data-ttu-id="e3c9b-114">Используйте метод **повторный запрос** для обновления все содержимое объекта **набора записей** из источника данных путем получения исходного команды и извлечение данных еще раз.</span><span class="sxs-lookup"><span data-stu-id="e3c9b-114">Use the **Requery** method to refresh the entire contents of a **Recordset** object from the data source by reissuing the original command and retrieving the data a second time.</span></span> <span data-ttu-id="e3c9b-115">Вызов данного метода эквивалентен вызову метода [Close](close-method-ado.md) и [открытия](open-method-ado-recordset.md) последовательно.</span><span class="sxs-lookup"><span data-stu-id="e3c9b-115">Calling this method is equivalent to calling the [Close](close-method-ado.md) and [Open](open-method-ado-recordset.md) methods in succession.</span></span> <span data-ttu-id="e3c9b-116">Если вы изменяете текущей записи или добавлять новую запись, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="e3c9b-116">If you are editing the current record or adding a new record, an error occurs.</span></span>

<span data-ttu-id="e3c9b-117">Когда открыт объекта **набора записей** , свойства, которые определяют характер курсор ([CursorType](cursortype-property-ado.md), [LockType для](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md)и т. д.) доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e3c9b-117">While the **Recordset** object is open, the properties that define the nature of the cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), and so forth) are read-only.</span></span> <span data-ttu-id="e3c9b-118">Таким образом метод **повторный запрос** можно только обновить курсора.</span><span class="sxs-lookup"><span data-stu-id="e3c9b-118">Thus, the **Requery** method can only refresh the current cursor.</span></span> <span data-ttu-id="e3c9b-119">Чтобы изменить свойства курсора и просмотреть результаты, необходимо использовать метод [Close](close-method-ado.md) , чтобы свойства становятся чтение и запись еще раз.</span><span class="sxs-lookup"><span data-stu-id="e3c9b-119">To change any of the cursor properties and view the results, you must use the [Close](close-method-ado.md) method so that the properties become read/write again.</span></span> <span data-ttu-id="e3c9b-120">Затем можно изменить значения свойств и вызвать метод [Open](open-method-ado-recordset.md) , чтобы снова открыть курсор.</span><span class="sxs-lookup"><span data-stu-id="e3c9b-120">You can then change the property settings and call the [Open](open-method-ado-recordset.md) method to reopen the cursor.</span></span>

