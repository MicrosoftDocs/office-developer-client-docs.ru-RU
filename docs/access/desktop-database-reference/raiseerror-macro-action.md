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
# <a name="raiseerror-macro-action"></a><span data-ttu-id="aa7fb-102">Макрокоманда RaiseError</span><span class="sxs-lookup"><span data-stu-id="aa7fb-102">RaiseError macro action</span></span>

<span data-ttu-id="aa7fb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa7fb-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="aa7fb-104">Действие **раисиррор** создает исключение, которое может быть обработано макрокомандой **[OnError](onerror-macro-action.md)** .</span><span class="sxs-lookup"><span data-stu-id="aa7fb-104">The **RaiseError** action throws an exception that can be handled by the **[OnError](onerror-macro-action.md)** macro action.</span></span>

> [!NOTE]
> <span data-ttu-id="aa7fb-105">Действие **раисиррор** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-105">The **RaiseError** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="aa7fb-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="aa7fb-106">Setting</span></span>

<span data-ttu-id="aa7fb-107">Макрокоманда **раисиррор** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-107">The **RaiseError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa7fb-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="aa7fb-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="aa7fb-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="aa7fb-109">Required</span></span></p></th>
<th><p><span data-ttu-id="aa7fb-110">Описание</span><span class="sxs-lookup"><span data-stu-id="aa7fb-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa7fb-111">Номер ошибки</span><span class="sxs-lookup"><span data-stu-id="aa7fb-111">Error Number</span></span></p></td>
<td><p><span data-ttu-id="aa7fb-112">Да</span><span class="sxs-lookup"><span data-stu-id="aa7fb-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="aa7fb-113">Число или выражение, которое разрешается в тип данных Long.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-113">A number or an expression that resolves to the Long data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa7fb-114">Описание ошибки</span><span class="sxs-lookup"><span data-stu-id="aa7fb-114">Error Description</span></span></p></td>
<td><p><span data-ttu-id="aa7fb-115">Нет</span><span class="sxs-lookup"><span data-stu-id="aa7fb-115">No</span></span></p></td>
<td><p><span data-ttu-id="aa7fb-116">Строковое выражение, описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-116">A string expression that describes the error.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="aa7fb-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa7fb-117">Remarks</span></span>

<span data-ttu-id="aa7fb-118">Если действие **раисиррор** вызывается в событии **[перед изменением](before-change-macro-event.md)** или **[перед удалением](before-delete-macro-event.md)** макроса, событие отменяется.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-118">If the **RaiseError** action is called in a **[Before Change](before-change-macro-event.md)** or **[Before Delete](before-delete-macro-event.md)** macro event, the event is cancelled.</span></span>

<span data-ttu-id="aa7fb-119">Если отсутствует активный оператор **OnError** , который обрабатывает ошибки, то ошибка, вызываемая действием **раисиррор** , добавляется в системную таблицу **усисаппликатионлог** .</span><span class="sxs-lookup"><span data-stu-id="aa7fb-119">If there is not an active **OnError** statment that is handling errors, then the error thrown by the **RaiseError** action is added to the **USysApplicationLog** system table.</span></span> <span data-ttu-id="aa7fb-120">При выполнении действия **раисиррор** для записи в таблицу **Усисаппликатионлог** для столбца **Category** автоматически устанавливается значение **выполнение**.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-120">When the **RaiseError** action to writes to the **USysApplicationLog** table, the **Category** column is automatically set to **Execution**.</span></span>

<span data-ttu-id="aa7fb-121">Чтобы просмотреть таблицу **усисаппликатионлог** , выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-121">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="aa7fb-122">Откройте меню **файл** и выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-122">Click the **File** menu, and then click **Options**.</span></span>

2.  <span data-ttu-id="aa7fb-123">В диалоговом окне **Параметры Access** перейдите на вкладку **Текущая база данных** .</span><span class="sxs-lookup"><span data-stu-id="aa7fb-123">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="aa7fb-124">В разделе **Навигация** щелкните **Параметры навигации**.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-124">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="aa7fb-125">В диалоговом окне **Параметры навигации** нажмите кнопку **Показать системные объекты**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-125">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="aa7fb-126">Нажмите кнопку **ОК** , чтобы закрыть диалоговое окно **Параметры Access** .</span><span class="sxs-lookup"><span data-stu-id="aa7fb-126">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="aa7fb-127">Пример</span><span class="sxs-lookup"><span data-stu-id="aa7fb-127">Example</span></span>

<span data-ttu-id="aa7fb-128">В приведенном ниже примере показано, как использовать действие Раисиррор для отмены события перед изменением данных макроса.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-128">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="aa7fb-129">При обновлении поля AssignedTo используется блок данных LookupRecord, чтобы определить, назначен ли назначенному специалисту открытый запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-129">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="aa7fb-130">Если этот параметр имеет значение true, то событие "до изменения" отменяется и запись не обновляется.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-130">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="aa7fb-131">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="aa7fb-131">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
