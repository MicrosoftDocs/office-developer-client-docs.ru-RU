---
title: Блок данных макрокомандой НайтиЗапись, после
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c93f312dd9b43a3235f049b9e6d3f95d08eba87f
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025597"
---
# <a name="lookuprecord-data-block"></a><span data-ttu-id="359b9-102">Блок данных макрокомандой НайтиЗапись, после</span><span class="sxs-lookup"><span data-stu-id="359b9-102">LookupRecord data block</span></span>

<span data-ttu-id="359b9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="359b9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="359b9-104">Блок данных **макрокомандой НайтиЗапись, после** выполняет набор действий в конкретной записи.</span><span class="sxs-lookup"><span data-stu-id="359b9-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span>

> [!NOTE]
> <span data-ttu-id="359b9-105">Блок данных **макрокомандой НайтиЗапись, после** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="359b9-105">The **LookupRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="359b9-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="359b9-106">Setting</span></span>

<span data-ttu-id="359b9-107">Действие **SetField** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="359b9-107">The **SetField** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="359b9-108">Argument</span><span class="sxs-lookup"><span data-stu-id="359b9-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="359b9-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="359b9-109">Required</span></span></p></th>
<th><p><span data-ttu-id="359b9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="359b9-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="359b9-111">Куда включается</span><span class="sxs-lookup"><span data-stu-id="359b9-111">In</span></span></p></td>
<td><p><span data-ttu-id="359b9-112">Да</span><span class="sxs-lookup"><span data-stu-id="359b9-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="359b9-113">Строка, идентифицирующая запись для работы.</span><span class="sxs-lookup"><span data-stu-id="359b9-113">A string that identifies the record to operate on.</span></span> <span data-ttu-id="359b9-114">Аргумент <em>в</em> может содержать имя таблицы, запроса или инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="359b9-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="359b9-115"><strong>Примечание</strong>: указанной записи не может содержать данные, хранящиеся в связанной таблице или источник данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="359b9-115"><strong>NOTE</strong>: The specified record cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="359b9-116">Условие отбора</span><span class="sxs-lookup"><span data-stu-id="359b9-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="359b9-117">Нет</span><span class="sxs-lookup"><span data-stu-id="359b9-117">No</span></span></p></td>
<td><p><span data-ttu-id="359b9-118">Строковое выражение, используемое для ограничения диапазона данных, на котором блок данных <strong>макрокомандой НайтиЗапись, после</strong> выполнения.</span><span class="sxs-lookup"><span data-stu-id="359b9-118">A string expression used to restrict the range of data on which the <strong>LookupRecord</strong> data block is performed.</span></span> <span data-ttu-id="359b9-119">К примеру, критерии эквивалентны часто предложение WHERE в выражении SQL без слова ГДЕ.</span><span class="sxs-lookup"><span data-stu-id="359b9-119">For example, criteria are often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="359b9-120">Если критерии опускаются, блок данных <strong>макрокомандой НайтиЗапись, после</strong> действует на весь домен, указанный в аргументе <em>в</em> .</span><span class="sxs-lookup"><span data-stu-id="359b9-120">If criteria are omitted, the <strong>LookupRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="359b9-121">Поля, который включен в условия также должны входить в <em>в</em>поле.</span><span class="sxs-lookup"><span data-stu-id="359b9-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="359b9-122">псевдоним;</span><span class="sxs-lookup"><span data-stu-id="359b9-122">Alias</span></span></p></td>
<td><p><span data-ttu-id="359b9-123">Нет</span><span class="sxs-lookup"><span data-stu-id="359b9-123">No</span></span></p></td>
<td><p><span data-ttu-id="359b9-124">Строка, которая предоставляет альтернативное имя для записи, указанный в аргументе <em>в</em> .</span><span class="sxs-lookup"><span data-stu-id="359b9-124">A string that provides an alternative name for the record specified by the <em>In</em> argument.</span></span> <span data-ttu-id="359b9-125">Позволяет сократить имя таблицы для последующих ссылок избежать возможных неоднозначных ссылок.</span><span class="sxs-lookup"><span data-stu-id="359b9-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="359b9-126">Если <em>псевдоним</em> не указан, будут использовать имя таблицы или запроса в качестве псевдоним.</span><span class="sxs-lookup"><span data-stu-id="359b9-126">If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="359b9-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="359b9-127">Remarks</span></span>

<span data-ttu-id="359b9-128">Если условиям, указанным *в* и *Где условие* аргументы указывает более одной записи, блок данных **макрокомандой НайтиЗапись, после** будет работать только на первой записи.</span><span class="sxs-lookup"><span data-stu-id="359b9-128">If the criteria specified by the *In* and *Where Condition* arguments specifies more than one record, the **LookupRecord** data block will operate only on the first record.</span></span>

## <a name="example"></a><span data-ttu-id="359b9-129">Пример</span><span class="sxs-lookup"><span data-stu-id="359b9-129">Example</span></span>

<span data-ttu-id="359b9-130">Следующий пример демонстрирует действие SetReturnVar используется для возврата значения из именованный макрос данных.</span><span class="sxs-lookup"><span data-stu-id="359b9-130">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="359b9-131">ReturnVar, с именем **CurrentServiceRequest** возвращается в макросе или Visual Basic для приложений (VBA) подпрограмму, которая называется именованный макрос данных.</span><span class="sxs-lookup"><span data-stu-id="359b9-131">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="359b9-132">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="359b9-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```

<br/>

<span data-ttu-id="359b9-133">Следующем примере показано, как использовать действие RaiseError для отмены события макрос данных до изменения.</span><span class="sxs-lookup"><span data-stu-id="359b9-133">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="359b9-134">При обновлении поля Кому назначено блок данных макрокомандой НайтиЗапись, после используется для определения, назначенный технического специалиста в настоящее время назначен ли запроса на открытие службы.</span><span class="sxs-lookup"><span data-stu-id="359b9-134">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="359b9-135">Если это так, отмене события до изменения и запись не обновляется.</span><span class="sxs-lookup"><span data-stu-id="359b9-135">If this is true, the Before Change event is cancelled and the record is not updated.</span></span>

```vb
    /* Get the name of the technician  */
    Look Up A Record In tblTechnicians
        Where Condition =[tblTechnicians].[ID]=[tblServiceRequests].[AssignedTo]
    SetLocalVar
        Name TechName
        Expression [tblTechnicians].[FirstName] & " " & [tblTechnicians].[LastName]
    /* End LookUpRecord  */
    
    If Updated("AssignedTo") Then
        Look Up A Record In tblServiceRequests
            Where Condition SR.[AssignedTo]=tblServiceRequests[AssignedTo] And 
                SR.[ID]<>tblServiceRequests.[ID] And IsNull(SR.[ActualCompletionDate])
            Alias SR
            RaiseError
                Error Number 1234
                Error Description ="Cannot assign a request to the specified technician: " & [TechName]
    
    End If
```
