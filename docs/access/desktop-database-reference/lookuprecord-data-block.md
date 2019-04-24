---
title: Блок данных LookupRecord
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 920f0830a310452962eb5dd1c21be63215bf0f03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289793"
---
# <a name="lookuprecord-data-block"></a><span data-ttu-id="b70e9-102">Блок данных LookupRecord</span><span class="sxs-lookup"><span data-stu-id="b70e9-102">LookupRecord data block</span></span>

<span data-ttu-id="b70e9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b70e9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b70e9-104">Блок данных **LookupRecord** выполняет набор действий с определенной записью.</span><span class="sxs-lookup"><span data-stu-id="b70e9-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span>

> [!NOTE]
> <span data-ttu-id="b70e9-105">Блок данных **LookupRecord** доступен только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="b70e9-105">The **LookupRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="b70e9-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="b70e9-106">Setting</span></span>

<span data-ttu-id="b70e9-107">Макрокоманда **SetField** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="b70e9-107">The **SetField** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b70e9-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="b70e9-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="b70e9-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b70e9-109">Required</span></span></p></th>
<th><p><span data-ttu-id="b70e9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b70e9-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b70e9-111">Куда включается</span><span class="sxs-lookup"><span data-stu-id="b70e9-111">In</span></span></p></td>
<td><p><span data-ttu-id="b70e9-112">Да</span><span class="sxs-lookup"><span data-stu-id="b70e9-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="b70e9-113">Строка, определяющая запись, с которой выполняется работа.</span><span class="sxs-lookup"><span data-stu-id="b70e9-113">A string that identifies the record to operate on.</span></span> <span data-ttu-id="b70e9-114">Аргумент <em>in</em> может содержать имя таблицы, запрос на выборку или инструкцию SQL.</span><span class="sxs-lookup"><span data-stu-id="b70e9-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="b70e9-115"><strong>Note</strong>: указанная запись не может содержать данные, хранящиеся в связанной таблице или источнике данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="b70e9-115"><strong>NOTE</strong>: The specified record cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b70e9-116">Условие отбора</span><span class="sxs-lookup"><span data-stu-id="b70e9-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="b70e9-117">Нет</span><span class="sxs-lookup"><span data-stu-id="b70e9-117">No</span></span></p></td>
<td><p><span data-ttu-id="b70e9-118">Строковое выражение, используемое для ограничения диапазона данных, в котором выполняется блок данных <strong>LookupRecord</strong> .</span><span class="sxs-lookup"><span data-stu-id="b70e9-118">A string expression used to restrict the range of data on which the <strong>LookupRecord</strong> data block is performed.</span></span> <span data-ttu-id="b70e9-119">Например, критерии часто эквивалентны предложению WHERE в выражении SQL, без слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="b70e9-119">For example, criteria are often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="b70e9-120">Если критерии опущены, блок данных <strong>LookupRecord</strong> работает на всем домене, указанном аргументом <em>in</em> .</span><span class="sxs-lookup"><span data-stu-id="b70e9-120">If criteria are omitted, the <strong>LookupRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="b70e9-121">Все поля, включенные в критерии, также должны быть полями в <em></em>.</span><span class="sxs-lookup"><span data-stu-id="b70e9-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b70e9-122">Alias</span><span class="sxs-lookup"><span data-stu-id="b70e9-122">Alias</span></span></p></td>
<td><p><span data-ttu-id="b70e9-123">Нет</span><span class="sxs-lookup"><span data-stu-id="b70e9-123">No</span></span></p></td>
<td><p><span data-ttu-id="b70e9-124">Строка, предоставляющая альтернативное имя для записи, заданной аргументом <em>in</em> .</span><span class="sxs-lookup"><span data-stu-id="b70e9-124">A string that provides an alternative name for the record specified by the <em>In</em> argument.</span></span> <span data-ttu-id="b70e9-125">Часто используется для сокращения имени таблицы для последующих ссылок, чтобы предотвратить возможные неоднозначные ссылки.</span><span class="sxs-lookup"><span data-stu-id="b70e9-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="b70e9-126">Если параметр <em>Alias</em> не указан, имя таблицы или запроса будет использоваться в качестве псевдонима.</span><span class="sxs-lookup"><span data-stu-id="b70e9-126">If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b70e9-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="b70e9-127">Remarks</span></span>

<span data-ttu-id="b70e9-128">Если условие, заданное в аргументах *условия* *in* и WHERE, указывает более одной записи, блок данных **LookupRecord** будет работать только с первой записью.</span><span class="sxs-lookup"><span data-stu-id="b70e9-128">If the criteria specified by the *In* and *Where Condition* arguments specifies more than one record, the **LookupRecord** data block will operate only on the first record.</span></span>

## <a name="example"></a><span data-ttu-id="b70e9-129">Пример</span><span class="sxs-lookup"><span data-stu-id="b70e9-129">Example</span></span>

<span data-ttu-id="b70e9-130">В приведенном ниже примере показано, как с помощью действия SetReturnVar вернуть значение из именованного макроса данных.</span><span class="sxs-lookup"><span data-stu-id="b70e9-130">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="b70e9-131">ReturnVar с именем **куррентсервицерекуест** возвращается в макрос или подПрограмму Visual Basic для приложений (VBA), которая вызвала именованный макрос данных.</span><span class="sxs-lookup"><span data-stu-id="b70e9-131">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="b70e9-132">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="b70e9-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<span data-ttu-id="b70e9-133">В приведенном ниже примере показано, как использовать действие Раисиррор для отмены события перед изменением данных макроса.</span><span class="sxs-lookup"><span data-stu-id="b70e9-133">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="b70e9-134">При обновлении поля AssignedTo используется блок данных LookupRecord, чтобы определить, назначен ли назначенному специалисту открытый запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="b70e9-134">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="b70e9-135">Если этот параметр имеет значение true, событие "до изменения" отменяется и запись не обновляется.</span><span class="sxs-lookup"><span data-stu-id="b70e9-135">If this is true, the Before Change event is cancelled and the record is not updated.</span></span>

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
