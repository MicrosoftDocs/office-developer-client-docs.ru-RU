---
title: Requery Method (ADO)
TOCTitle: Requery Method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3fde13d923a67ca995cdb3e7f59a327e82a9688
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481805"
---
# <a name="requery-method-ado"></a><span data-ttu-id="7c0f1-102">Requery Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="7c0f1-102">Requery Method (ADO)</span></span>


<span data-ttu-id="7c0f1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c0f1-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="7c0f1-104">Обновляет данные в объект [набора записей](recordset-object-ado.md) , повторное выполнение запросов, на котором основан объект.</span><span class="sxs-lookup"><span data-stu-id="7c0f1-104">Updates the data in a [Recordset](recordset-object-ado.md) object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c0f1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c0f1-105">Syntax</span></span>

<span data-ttu-id="7c0f1-106">*набор записей*. Обновление *параметров*</span><span class="sxs-lookup"><span data-stu-id="7c0f1-106">*recordset*.Requery *Options*</span></span>

## <a name="parameter"></a><span data-ttu-id="7c0f1-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="7c0f1-107">Parameter</span></span>

  - <span data-ttu-id="7c0f1-108">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="7c0f1-108">*Options*</span></span>

  - <span data-ttu-id="7c0f1-109">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="7c0f1-109">Optional.</span></span> <span data-ttu-id="7c0f1-110">Битовая маска, которая содержит значения [ExecuteOptionEnum](executeoptionenum.md) и [CommandTypeEnum](commandtypeenum.md) влияния на этой операции.</span><span class="sxs-lookup"><span data-stu-id="7c0f1-110">A bitmask that contains [ExecuteOptionEnum](executeoptionenum.md) and [CommandTypeEnum](commandtypeenum.md) values affecting this operation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7c0f1-111">Если <EM>Параметры</EM> <STRONG>adAsyncExecute</STRONG>, эта операция выполняется асинхронно и события <A href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</A> будет выдается, когда она завершается.</span><span class="sxs-lookup"><span data-stu-id="7c0f1-111">If <EM>Options</EM> is set to <STRONG>adAsyncExecute</STRONG>, this operation will execute asynchronously and a <A href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</A> event will be issued when it concludes.</span></span></P>



<span data-ttu-id="7c0f1-112">Значения **ExecuteOpenEnum** **adExecuteNoRecords** или **adExecuteStream** не должен использоваться с **повторный запрос**.</span><span class="sxs-lookup"><span data-stu-id="7c0f1-112">The **ExecuteOpenEnum** values of **adExecuteNoRecords** or **adExecuteStream** should not be used with **Requery**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c0f1-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="7c0f1-113">Remarks</span></span>

<span data-ttu-id="7c0f1-114">Используйте метод **повторный запрос** для обновления все содержимое объекта **набора записей** из источника данных путем получения исходного команды и извлечение данных еще раз.</span><span class="sxs-lookup"><span data-stu-id="7c0f1-114">Use the **Requery** method to refresh the entire contents of a **Recordset** object from the data source by reissuing the original command and retrieving the data a second time.</span></span> <span data-ttu-id="7c0f1-115">Вызов данного метода эквивалентен вызову метода [Close](close-method-ado.md) и [открытия](open-method-ado-recordset.md) последовательно.</span><span class="sxs-lookup"><span data-stu-id="7c0f1-115">Calling this method is equivalent to calling the [Close](close-method-ado.md) and [Open](open-method-ado-recordset.md) methods in succession.</span></span> <span data-ttu-id="7c0f1-116">Если вы изменяете текущей записи или добавлять новую запись, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="7c0f1-116">If you are editing the current record or adding a new record, an error occurs.</span></span>

<span data-ttu-id="7c0f1-117">Когда открыт объекта **набора записей** , свойства, которые определяют характер курсор ([CursorType](cursortype-property-ado.md), [LockType для](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md)и т. д.) доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7c0f1-117">While the **Recordset** object is open, the properties that define the nature of the cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), and so forth) are read-only.</span></span> <span data-ttu-id="7c0f1-118">Таким образом метод **повторный запрос** можно только обновить курсора.</span><span class="sxs-lookup"><span data-stu-id="7c0f1-118">Thus, the **Requery** method can only refresh the current cursor.</span></span> <span data-ttu-id="7c0f1-119">Чтобы изменить свойства курсора и просмотреть результаты, необходимо использовать метод [Close](close-method-ado.md) , чтобы свойства становятся чтение и запись еще раз.</span><span class="sxs-lookup"><span data-stu-id="7c0f1-119">To change any of the cursor properties and view the results, you must use the [Close](close-method-ado.md) method so that the properties become read/write again.</span></span> <span data-ttu-id="7c0f1-120">Затем можно изменить значения свойств и вызвать метод [Open](open-method-ado-recordset.md) , чтобы снова открыть курсор.</span><span class="sxs-lookup"><span data-stu-id="7c0f1-120">You can then change the property settings and call the [Open](open-method-ado-recordset.md) method to reopen the cursor.</span></span>

