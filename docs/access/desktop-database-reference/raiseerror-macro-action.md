---
title: Макрокоманда RaiseError
TOCTitle: RaiseError macro action
ms:assetid: c8c57685-b373-67d6-cea6-8f2c334547d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823192(v=office.15)
ms:contentKeyID: 48547661
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b706ffed14fdb440f3c3192c7c36015343f2e134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300926"
---
# <a name="raiseerror-macro-action"></a><span data-ttu-id="0661d-102">Макрокоманда RaiseError</span><span class="sxs-lookup"><span data-stu-id="0661d-102">RaiseError macro action</span></span>

<span data-ttu-id="0661d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0661d-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="0661d-104">Действие **RaiseError** бросает исключение, которое может быть обработано макро-действием **[OnError.](onerror-macro-action.md)**</span><span class="sxs-lookup"><span data-stu-id="0661d-104">The **RaiseError** action throws an exception that can be handled by the **[OnError](onerror-macro-action.md)** macro action.</span></span>

> [!NOTE]
> <span data-ttu-id="0661d-105">Действие **RaiseError** доступно только в Макросах данных.</span><span class="sxs-lookup"><span data-stu-id="0661d-105">The **RaiseError** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="0661d-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="0661d-106">Setting</span></span>

<span data-ttu-id="0661d-107">Действие **RaiseError имеет** следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="0661d-107">The **RaiseError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0661d-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="0661d-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="0661d-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0661d-109">Required</span></span></p></th>
<th><p><span data-ttu-id="0661d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0661d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0661d-111">Номер ошибки</span><span class="sxs-lookup"><span data-stu-id="0661d-111">Error Number</span></span></p></td>
<td><p><span data-ttu-id="0661d-112">Да</span><span class="sxs-lookup"><span data-stu-id="0661d-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="0661d-113">Число или выражение, разрешаемая типу Длинные данные.</span><span class="sxs-lookup"><span data-stu-id="0661d-113">A number or an expression that resolves to the Long data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0661d-114">Описание ошибки</span><span class="sxs-lookup"><span data-stu-id="0661d-114">Error Description</span></span></p></td>
<td><p><span data-ttu-id="0661d-115">Нет</span><span class="sxs-lookup"><span data-stu-id="0661d-115">No</span></span></p></td>
<td><p><span data-ttu-id="0661d-116">Строка, описываемая ошибкой.</span><span class="sxs-lookup"><span data-stu-id="0661d-116">A string expression that describes the error.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0661d-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="0661d-117">Remarks</span></span>

<span data-ttu-id="0661d-118">Если действие **RaiseError** вызывается **[](before-change-macro-event.md)** в **[](before-delete-macro-event.md)** событии перед изменением или перед удалением макросов, событие отменяется.</span><span class="sxs-lookup"><span data-stu-id="0661d-118">If the **RaiseError** action is called in a **[Before Change](before-change-macro-event.md)** or **[Before Delete](before-delete-macro-event.md)** macro event, the event is cancelled.</span></span>

<span data-ttu-id="0661d-119">Если не существует активного заявления **OnError,** которое занимается ошибками, ошибка, брошенная действием **RaiseError,** добавляется в таблицу **системы USysApplicationLog.**</span><span class="sxs-lookup"><span data-stu-id="0661d-119">If there is not an active **OnError** statment that is handling errors, then the error thrown by the **RaiseError** action is added to the **USysApplicationLog** system table.</span></span> <span data-ttu-id="0661d-120">Когда действие **RaiseError** для записи в таблицу **USysApplicationLog** автоматически задает столбец **Category** **к исполнению**.</span><span class="sxs-lookup"><span data-stu-id="0661d-120">When the **RaiseError** action to writes to the **USysApplicationLog** table, the **Category** column is automatically set to **Execution**.</span></span>

<span data-ttu-id="0661d-121">Чтобы увидеть **таблицу USysApplicationLog,** используйте следующие действия:</span><span class="sxs-lookup"><span data-stu-id="0661d-121">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="0661d-122">Щелкните **меню File** и нажмите кнопку **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="0661d-122">Click the **File** menu, and then click **Options**.</span></span>

2.  <span data-ttu-id="0661d-123">В **диалоговом окне Параметры** доступа щелкните вкладку **Current Database.**</span><span class="sxs-lookup"><span data-stu-id="0661d-123">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="0661d-124">В разделе **Навигация** нажмите **кнопку Параметры навигации**.</span><span class="sxs-lookup"><span data-stu-id="0661d-124">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="0661d-125">В **диалоговом окне Параметры** навигации щелкните **Показать объекты системы** и нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="0661d-125">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="0661d-126">Нажмите **кнопку ОК,** чтобы **отклонять диалоговое** окно Access Options.</span><span class="sxs-lookup"><span data-stu-id="0661d-126">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="0661d-127">Пример</span><span class="sxs-lookup"><span data-stu-id="0661d-127">Example</span></span>

<span data-ttu-id="0661d-128">В следующем примере показано, как использовать действие RaiseError для отмены макрос события перед изменением данных.</span><span class="sxs-lookup"><span data-stu-id="0661d-128">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="0661d-129">При обновлении поля AssignedTo блок данных LookupRecord используется для определения того, назначен ли назначенный специалист в настоящее время запросу открытой службы.</span><span class="sxs-lookup"><span data-stu-id="0661d-129">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="0661d-130">Если это так, событие Before Change отменяется и запись не обновляется.</span><span class="sxs-lookup"><span data-stu-id="0661d-130">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="0661d-131">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="0661d-131">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
