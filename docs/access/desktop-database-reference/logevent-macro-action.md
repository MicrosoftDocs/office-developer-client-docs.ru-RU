---
title: LogEvent Macro Action
TOCTitle: LogEvent Macro Action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f626dd61782baed2e46aa931891a172fc53c1bde
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481851"
---
# <a name="logevent-macro-action"></a><span data-ttu-id="4ec08-102">LogEvent Macro Action</span><span class="sxs-lookup"><span data-stu-id="4ec08-102">LogEvent Macro Action</span></span>


<span data-ttu-id="4ec08-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ec08-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4ec08-104">Действие **LogEvent** записывает сведения об **системы см** .</span><span class="sxs-lookup"><span data-stu-id="4ec08-104">The **LogEvent** action writes information to the **USysApplicationLog** system table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4ec08-105"><STRONG>LogEvent</STRONG> действие доступно только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="4ec08-105">The <STRONG>LogEvent</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="4ec08-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="4ec08-106">Setting</span></span>

<span data-ttu-id="4ec08-107">Действие **LogEvent** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="4ec08-107">The **LogEvent** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ec08-108">Argument</span><span class="sxs-lookup"><span data-stu-id="4ec08-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="4ec08-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4ec08-109">Required</span></span></p></th>
<th><p><span data-ttu-id="4ec08-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4ec08-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ec08-111"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="4ec08-111"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="4ec08-112">НЕТ</span><span class="sxs-lookup"><span data-stu-id="4ec08-112">No</span></span></p></td>
<td><p><span data-ttu-id="4ec08-113">Строковое выражение, описывающее условие, следует регистрировать.</span><span class="sxs-lookup"><span data-stu-id="4ec08-113">A string expression that describes the condition that you want to log.</span></span> <span data-ttu-id="4ec08-114">Описание не может превышать 255 знаков.</span><span class="sxs-lookup"><span data-stu-id="4ec08-114">The description cannot exceed 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4ec08-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="4ec08-115">Remarks</span></span>

<span data-ttu-id="4ec08-116">Действие **LogEvent** можно использовать для записи сведений о состоянии **, не никак с помощью действия **[RaiseError](raiseerror-macro-action.md)** приводит к возникновению ошибки системы см** .</span><span class="sxs-lookup"><span data-stu-id="4ec08-116">The **LogEvent** action can be used to write status information to the **USysApplicationLog** system table that does not merit using the **[RaiseError](raiseerror-macro-action.md)** action to throw an error.</span></span> <span data-ttu-id="4ec08-117">К примеру вы журнал изменений для определенного поля или использовать при отладке макрос с помощью элементов в **USysApplicationLog** .</span><span class="sxs-lookup"><span data-stu-id="4ec08-117">For example, you could log changes to a specific field, or use the items written to the **USysApplicationLog** to assist you in debugging your macro.</span></span>

<span data-ttu-id="4ec08-118">При использовании **LogEvent** действие для записи **см** в столбце **категории** автоматически устанавливается значение **пользователя**.</span><span class="sxs-lookup"><span data-stu-id="4ec08-118">When you use the **LogEvent** action to write to the **USysApplicationLog** table, the **Category** column is automatically set to **User**.</span></span>

<span data-ttu-id="4ec08-119">Чтобы просмотреть **сведения см** , выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4ec08-119">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="4ec08-120">Выберите в меню **файл** и выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="4ec08-120">Click the **File** menu,and then click **Options**.</span></span>

2.  <span data-ttu-id="4ec08-121">В диалоговом окне **Параметры доступа к** перейдите на вкладку **Текущей базы данных** .</span><span class="sxs-lookup"><span data-stu-id="4ec08-121">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="4ec08-122">В разделе **Переходы** щелкните **Параметры навигации**.</span><span class="sxs-lookup"><span data-stu-id="4ec08-122">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="4ec08-123">В диалоговом окне **Параметры навигации** нажмите кнопку **Показать системные объекты**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4ec08-123">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="4ec08-124">Нажмите **кнопку ОК** , чтобы закрыть диалоговое окно **Параметры доступа** .</span><span class="sxs-lookup"><span data-stu-id="4ec08-124">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

