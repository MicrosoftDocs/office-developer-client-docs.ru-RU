---
title: Блок данных LookupRecord
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7a5cccb77300f36f3e33cd1eccb6c6d278db3120
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734212"
---
# <a name="lookuprecord-data-block"></a><span data-ttu-id="1b76a-102">Блок данных LookupRecord</span><span class="sxs-lookup"><span data-stu-id="1b76a-102">LookupRecord data block</span></span>

<span data-ttu-id="1b76a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b76a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b76a-104">Блок **данных LookupRecord** выполняет набор действий с определенной записью.</span><span class="sxs-lookup"><span data-stu-id="1b76a-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span>

> [!NOTE]
> <span data-ttu-id="1b76a-105">Блок **данных LookupRecord** доступен только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="1b76a-105">The **LookupRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="1b76a-106">Setting</span><span class="sxs-lookup"><span data-stu-id="1b76a-106">Setting</span></span>

<span data-ttu-id="1b76a-107">Действие **SetField** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="1b76a-107">The **SetField** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1b76a-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="1b76a-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="1b76a-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1b76a-109">Required</span></span></p></th>
<th><p><span data-ttu-id="1b76a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1b76a-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b76a-111">Куда включается</span><span class="sxs-lookup"><span data-stu-id="1b76a-111">In</span></span></p></td>
<td><p><span data-ttu-id="1b76a-112">Да</span><span class="sxs-lookup"><span data-stu-id="1b76a-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="1b76a-113">Строка, идентифицирует запись, с которую необходимо работать.</span><span class="sxs-lookup"><span data-stu-id="1b76a-113">A string that identifies the record to operate on.</span></span> <span data-ttu-id="1b76a-114">Аргумент <em>In</em> может содержать имя таблицы, запрос выбора или SQL.</span><span class="sxs-lookup"><span data-stu-id="1b76a-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="1b76a-115"><strong>ПРИМЕЧАНИЕ.</strong>Указанная запись не может включать данные, хранимые в связанной таблице или источнике данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="1b76a-115"><strong>NOTE</strong>: The specified record cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b76a-116">Where Condition</span><span class="sxs-lookup"><span data-stu-id="1b76a-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="1b76a-117">Нет</span><span class="sxs-lookup"><span data-stu-id="1b76a-117">No</span></span></p></td>
<td><p><span data-ttu-id="1b76a-118">Строка выражения, используемая для ограничения диапазона данных, для которого выполняется блок данных <strong>LookupRecord.</strong></span><span class="sxs-lookup"><span data-stu-id="1b76a-118">A string expression used to restrict the range of data on which the <strong>LookupRecord</strong> data block is performed.</span></span> <span data-ttu-id="1b76a-119">Например, критерии часто эквивалентны предложению WHERE в SQL выражения без слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="1b76a-119">For example, criteria are often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="1b76a-120">Если критерии не указаны, блок данных <strong>LookupRecord</strong> работает на всем домене, указанном аргументом <em>In.</em></span><span class="sxs-lookup"><span data-stu-id="1b76a-120">If criteria are omitted, the <strong>LookupRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="1b76a-121">Любое поле, включенное в условия, также должно быть полем в <em>in</em>.</span><span class="sxs-lookup"><span data-stu-id="1b76a-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b76a-122">Alias</span><span class="sxs-lookup"><span data-stu-id="1b76a-122">Alias</span></span></p></td>
<td><p><span data-ttu-id="1b76a-123">Нет</span><span class="sxs-lookup"><span data-stu-id="1b76a-123">No</span></span></p></td>
<td><p><span data-ttu-id="1b76a-124">Строка, которая предоставляет альтернативное имя для записи, указанной в <em>аргументе In.</em></span><span class="sxs-lookup"><span data-stu-id="1b76a-124">A string that provides an alternative name for the record specified by the <em>In</em> argument.</span></span> <span data-ttu-id="1b76a-125">Часто используется для сокращения имени таблицы для последующих ссылок, чтобы предотвратить возможные неоднозначные ссылки.</span><span class="sxs-lookup"><span data-stu-id="1b76a-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="1b76a-126">Если <em>псевдоним не</em> указан, в качестве псевдонима будет использоваться таблица или имя запроса.</span><span class="sxs-lookup"><span data-stu-id="1b76a-126">If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1b76a-127">Заметки</span><span class="sxs-lookup"><span data-stu-id="1b76a-127">Remarks</span></span>

<span data-ttu-id="1b76a-128">Если критерии, указанные  аргументами условия "В" и "Где", возвращают несколько записей, блок данных **LookupRecord** будет работать только с первой записью. </span><span class="sxs-lookup"><span data-stu-id="1b76a-128">If the criteria specified by the *In* and *Where Condition* arguments returns more than one record, the **LookupRecord** data block will operate only on the first record.</span></span>  <span data-ttu-id="1b76a-129">Если записи не соответствуют заданным условиям, Access пропустит набор действий, содержащихся в блоке **LookupRecord,** как если бы это было выражение блока макроса **[If,](if-then-else-macro-block.md)** которое было оценено как false.</span><span class="sxs-lookup"><span data-stu-id="1b76a-129">In the case that no records match the specified criteria, Access will skip over the set of actions contained within the **LookupRecord** block, as if it had been an **[If](if-then-else-macro-block.md)** macro block expression that evaluated as false.</span></span>

## <a name="example"></a><span data-ttu-id="1b76a-130">Пример</span><span class="sxs-lookup"><span data-stu-id="1b76a-130">Example</span></span>

<span data-ttu-id="1b76a-131">В следующем примере показано, как использовать действие SetReturnVar для возврата значения из именоваемом макроса данных.</span><span class="sxs-lookup"><span data-stu-id="1b76a-131">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="1b76a-132">ReturnVar с **именем CurrentServiceRequest** возвращается в подгруппу макроса или Visual Basic для приложений (VBA), которая вызвала именуемого макроса данных.</span><span class="sxs-lookup"><span data-stu-id="1b76a-132">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="1b76a-133">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="1b76a-133">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<span data-ttu-id="1b76a-134">В следующем примере показано, как использовать действие RaiseError для отмены события макроса данных "Перед изменением".</span><span class="sxs-lookup"><span data-stu-id="1b76a-134">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="1b76a-135">При обновлении поля AssignedTo блок данных LookupRecord используется для определения того, назначен ли техники в настоящее время открытый запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="1b76a-135">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="1b76a-136">Если это так, событие before Change отменяется, а запись не обновляется.</span><span class="sxs-lookup"><span data-stu-id="1b76a-136">If this is true, the Before Change event is cancelled and the record is not updated.</span></span>

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
