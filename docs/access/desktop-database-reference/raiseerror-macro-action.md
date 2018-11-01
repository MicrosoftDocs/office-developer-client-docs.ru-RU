---
title: Действия макроса RaiseError
TOCTitle: RaiseError Macro Action
ms:assetid: c8c57685-b373-67d6-cea6-8f2c334547d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823192(v=office.15)
ms:contentKeyID: 48547661
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e7cddb3ace4027c2dba45fd685fbf16bd57b783e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887343"
---
# <a name="raiseerror-macro-action"></a><span data-ttu-id="647a6-102">Действия макроса RaiseError</span><span class="sxs-lookup"><span data-stu-id="647a6-102">RaiseError Macro Action</span></span>

<span data-ttu-id="647a6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="647a6-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="647a6-104">Действие **RaiseError** создает исключение, могут быть обработаны **[ПриОшибке](onerror-macro-action.md)** .</span><span class="sxs-lookup"><span data-stu-id="647a6-104">The **RaiseError** action throws an exception that can be handled by the **[OnError](onerror-macro-action.md)** macro action.</span></span>

> [!NOTE]
> <span data-ttu-id="647a6-105">Действие **RaiseError** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="647a6-105">The **RaiseError** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="647a6-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="647a6-106">Setting</span></span>

<span data-ttu-id="647a6-107">Действие **RaiseError** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="647a6-107">The **RaiseError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="647a6-108">Argument</span><span class="sxs-lookup"><span data-stu-id="647a6-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="647a6-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="647a6-109">Required</span></span></p></th>
<th><p><span data-ttu-id="647a6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="647a6-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="647a6-111">Номер ошибки</span><span class="sxs-lookup"><span data-stu-id="647a6-111">Error Number</span></span></p></td>
<td><p><span data-ttu-id="647a6-112">Да</span><span class="sxs-lookup"><span data-stu-id="647a6-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="647a6-113">Число или выражение, которое разрешается в тип данных Long.</span><span class="sxs-lookup"><span data-stu-id="647a6-113">A number or an expression that resolves to the Long data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="647a6-114">Описание ошибки</span><span class="sxs-lookup"><span data-stu-id="647a6-114">Error Description</span></span></p></td>
<td><p><span data-ttu-id="647a6-115">Нет</span><span class="sxs-lookup"><span data-stu-id="647a6-115">No</span></span></p></td>
<td><p><span data-ttu-id="647a6-116">Строковое выражение, описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="647a6-116">A string expression that describes the error.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="647a6-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="647a6-117">Remarks</span></span>

<span data-ttu-id="647a6-118">Если действие **RaiseError** вызывается в событии макрос **[До изменения](before-change-macro-event.md)** или **[До удаления](before-delete-macro-event.md)** , отмене события.</span><span class="sxs-lookup"><span data-stu-id="647a6-118">If the **RaiseError** action is called in a **[Before Change](before-change-macro-event.md)** or **[Before Delete](before-delete-macro-event.md)** macro event, the event is cancelled.</span></span>

<span data-ttu-id="647a6-119">Если не является активной инструкции **OnError** , который обрабатывает ошибки, ошибку, сгенерированную действие **RaiseError** добавляется к **системе см** .</span><span class="sxs-lookup"><span data-stu-id="647a6-119">If there is not an active **OnError** statment that is handling errors, then the error thrown by the **RaiseError** action is added to the **USysApplicationLog** system table.</span></span> <span data-ttu-id="647a6-120">Когда действие **RaiseError** записывает **сведения см** , в столбце **категории** автоматически устанавливается значение **выполнения**.</span><span class="sxs-lookup"><span data-stu-id="647a6-120">When the **RaiseError** action to writes to the **USysApplicationLog** table, the **Category** column is automatically set to **Execution**.</span></span>

<span data-ttu-id="647a6-121">Чтобы просмотреть **сведения см** , выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="647a6-121">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="647a6-122">Выберите в меню **файл** и выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="647a6-122">Click the **File** menu, and then click **Options**.</span></span>

2.  <span data-ttu-id="647a6-123">В диалоговом окне **Параметры доступа к** перейдите на вкладку **Текущей базы данных** .</span><span class="sxs-lookup"><span data-stu-id="647a6-123">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="647a6-124">В разделе **Переходы** щелкните **Параметры навигации**.</span><span class="sxs-lookup"><span data-stu-id="647a6-124">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="647a6-125">В диалоговом окне **Параметры навигации** нажмите кнопку **Показать системные объекты**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="647a6-125">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="647a6-126">Нажмите **кнопку ОК** , чтобы закрыть диалоговое окно **Параметры доступа** .</span><span class="sxs-lookup"><span data-stu-id="647a6-126">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="647a6-127">Пример</span><span class="sxs-lookup"><span data-stu-id="647a6-127">Example</span></span>

<span data-ttu-id="647a6-128">Следующем примере показано, как использовать действие RaiseError для отмены события макрос данных до изменения.</span><span class="sxs-lookup"><span data-stu-id="647a6-128">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="647a6-129">При обновлении поля Кому назначено блок данных макрокомандой НайтиЗапись, после используется для определения, назначенный технического специалиста в настоящее время назначен ли запроса на открытие службы.</span><span class="sxs-lookup"><span data-stu-id="647a6-129">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="647a6-130">Если это так, затем отмене события до изменения и запись не обновляется.</span><span class="sxs-lookup"><span data-stu-id="647a6-130">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="647a6-131">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="647a6-131">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
