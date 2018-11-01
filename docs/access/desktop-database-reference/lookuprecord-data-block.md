---
title: Блок данных LookupRecord
TOCTitle: LookupRecord Data Block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3bd9a687d7f74b99dc20ee079f970c37ba627f31
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877690"
---
# <a name="lookuprecord-data-block"></a><span data-ttu-id="68fd3-102">Блок данных LookupRecord</span><span class="sxs-lookup"><span data-stu-id="68fd3-102">LookupRecord Data Block</span></span>

<span data-ttu-id="68fd3-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="68fd3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="68fd3-104">Блок данных **макрокомандой НайтиЗапись, после** выполняет набор действий в конкретной записи.</span><span class="sxs-lookup"><span data-stu-id="68fd3-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span>

> [!NOTE]
> <span data-ttu-id="68fd3-105">Блок данных **макрокомандой НайтиЗапись, после** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="68fd3-105">The **LookupRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="68fd3-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="68fd3-106">Setting</span></span>

<span data-ttu-id="68fd3-107">Действие **SetField** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="68fd3-107">The **SetField** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="68fd3-108">Argument</span><span class="sxs-lookup"><span data-stu-id="68fd3-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="68fd3-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="68fd3-109">Required</span></span></p></th>
<th><p><span data-ttu-id="68fd3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="68fd3-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68fd3-111">Куда включается</span><span class="sxs-lookup"><span data-stu-id="68fd3-111">In</span></span></p></td>
<td><p><span data-ttu-id="68fd3-112">Да</span><span class="sxs-lookup"><span data-stu-id="68fd3-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="68fd3-113">Строка, идентифицирующая запись для работы.</span><span class="sxs-lookup"><span data-stu-id="68fd3-113">A string that identifies the record to operate on.</span></span> <span data-ttu-id="68fd3-114">Аргумент <em>в</em> может содержать имя таблицы, запроса или инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="68fd3-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p>

> [!NOTE]
> <span data-ttu-id="68fd3-115">Указанная запись не может включать данные, хранящиеся в связанной таблице или источник данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="68fd3-115">The specified record cannot include data stored in a linked table or ODBC data source.</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68fd3-116">Условие отбора</span><span class="sxs-lookup"><span data-stu-id="68fd3-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="68fd3-117">Нет</span><span class="sxs-lookup"><span data-stu-id="68fd3-117">No</span></span></p></td>
<td><p><span data-ttu-id="68fd3-118">Строковое выражение, используемое для ограничения диапазона данных, на котором блок данных <strong>макрокомандой НайтиЗапись, после</strong> выполнения.</span><span class="sxs-lookup"><span data-stu-id="68fd3-118">A string expression used to restrict the range of data on which the <strong>LookupRecord</strong> data block is performed.</span></span> <span data-ttu-id="68fd3-119">К примеру, критерии эквивалентны часто предложение WHERE в выражении SQL без слова ГДЕ.</span><span class="sxs-lookup"><span data-stu-id="68fd3-119">For example, criteria are often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="68fd3-120">Если критерии опускаются, блок данных <strong>макрокомандой НайтиЗапись, после</strong> действует на весь домен, указанный в аргументе <em>в</em> .</span><span class="sxs-lookup"><span data-stu-id="68fd3-120">If criteria are omitted, the <strong>LookupRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="68fd3-121">Поля, который включен в условия также должны входить в <em>в</em>поле.</span><span class="sxs-lookup"><span data-stu-id="68fd3-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68fd3-122">псевдоним;</span><span class="sxs-lookup"><span data-stu-id="68fd3-122">Alias</span></span></p></td>
<td><p><span data-ttu-id="68fd3-123">Нет</span><span class="sxs-lookup"><span data-stu-id="68fd3-123">No</span></span></p></td>
<td><p><span data-ttu-id="68fd3-124">Строка, которая предоставляет альтернативное имя для записи, указанный в аргументе <em>в</em> .</span><span class="sxs-lookup"><span data-stu-id="68fd3-124">A string that provides an alternative name for the record specified by the <em>In</em> argument.</span></span> <span data-ttu-id="68fd3-125">Позволяет сократить имя таблицы для последующих ссылок избежать возможных неоднозначных ссылок.</span><span class="sxs-lookup"><span data-stu-id="68fd3-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="68fd3-126">Если <em>псевдоним</em> не указан, будут использовать имя таблицы или запроса в качестве псевдоним.</span><span class="sxs-lookup"><span data-stu-id="68fd3-126">If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="68fd3-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="68fd3-127">Remarks</span></span>

<span data-ttu-id="68fd3-128">Если условиям, указанным *в* и *Где условие* аргументы указывает более одной записи, блок данных **макрокомандой НайтиЗапись, после** будет работать только на первой записи.</span><span class="sxs-lookup"><span data-stu-id="68fd3-128">If the criteria specified by the *In* and *Where Condition* arguments specifies more than one record, the **LookupRecord** data block will operate only on the first record.</span></span>

## <a name="example"></a><span data-ttu-id="68fd3-129">Пример</span><span class="sxs-lookup"><span data-stu-id="68fd3-129">Example</span></span>

<span data-ttu-id="68fd3-130">Следующий пример демонстрирует действие SetReturnVar используется для возврата значения из именованный макрос данных.</span><span class="sxs-lookup"><span data-stu-id="68fd3-130">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="68fd3-131">ReturnVar, с именем **CurrentServiceRequest** возвращается в макросе или Visual Basic для приложений (VBA) подпрограмму, которая называется именованный макрос данных.</span><span class="sxs-lookup"><span data-stu-id="68fd3-131">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="68fd3-132">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="68fd3-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<span data-ttu-id="68fd3-133">Следующем примере показано, как использовать действие RaiseError для отмены события макрос данных до изменения.</span><span class="sxs-lookup"><span data-stu-id="68fd3-133">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="68fd3-134">При обновлении поля Кому назначено блок данных макрокомандой НайтиЗапись, после используется для определения, назначенный технического специалиста в настоящее время назначен ли запроса на открытие службы.</span><span class="sxs-lookup"><span data-stu-id="68fd3-134">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="68fd3-135">Если это так, отмене события до изменения и запись не обновляется.</span><span class="sxs-lookup"><span data-stu-id="68fd3-135">If this is true, the Before Change event is cancelled and the record is not updated.</span></span>

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
