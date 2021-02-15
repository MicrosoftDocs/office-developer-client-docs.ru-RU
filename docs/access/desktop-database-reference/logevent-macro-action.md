---
title: Макрокоманда LogEvent
TOCTitle: LogEvent macro action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4106e66074975f08a5058aafbfc0c6deac156277
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289838"
---
# <a name="logevent-macro-action"></a><span data-ttu-id="8da19-102">Макрокоманда LogEvent</span><span class="sxs-lookup"><span data-stu-id="8da19-102">LogEvent macro action</span></span>

<span data-ttu-id="8da19-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8da19-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8da19-104">Действие **LogEvent** записывает сведения в системную таблицу **USysApplicationLog.**</span><span class="sxs-lookup"><span data-stu-id="8da19-104">The **LogEvent** action writes information to the **USysApplicationLog** system table.</span></span>

> [!NOTE]
> <span data-ttu-id="8da19-105">Действие **LogEvent** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="8da19-105">The **LogEvent** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="8da19-106">Setting</span><span class="sxs-lookup"><span data-stu-id="8da19-106">Setting</span></span>

<span data-ttu-id="8da19-107">Действие **LogEvent** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="8da19-107">The **LogEvent** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8da19-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="8da19-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="8da19-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8da19-109">Required</span></span></p></th>
<th><p><span data-ttu-id="8da19-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8da19-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8da19-111"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="8da19-111"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="8da19-112">Нет</span><span class="sxs-lookup"><span data-stu-id="8da19-112">No</span></span></p></td>
<td><p><span data-ttu-id="8da19-113">Строка выражения, описывая условие, которое необходимо занося в журнал.</span><span class="sxs-lookup"><span data-stu-id="8da19-113">A string expression that describes the condition that you want to log.</span></span> <span data-ttu-id="8da19-114">Описание не может превышать 255 символов.</span><span class="sxs-lookup"><span data-stu-id="8da19-114">The description cannot exceed 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="8da19-115">Заметки</span><span class="sxs-lookup"><span data-stu-id="8da19-115">Remarks</span></span>

<span data-ttu-id="8da19-116">Действие **LogEvent** можно использовать для записи сведений о состоянии в системную таблицу **USysApplicationLog,** которая не вызывает ошибку с помощью действия **[RaiseError.](raiseerror-macro-action.md)**</span><span class="sxs-lookup"><span data-stu-id="8da19-116">The **LogEvent** action can be used to write status information to the **USysApplicationLog** system table that does not merit using the **[RaiseError](raiseerror-macro-action.md)** action to throw an error.</span></span> <span data-ttu-id="8da19-117">Например, можно занести изменения в определенное поле или использовать элементы, написанные в **USysApplicationLog,** для отладки макроса.</span><span class="sxs-lookup"><span data-stu-id="8da19-117">For example, you could log changes to a specific field, or use the items written to the **USysApplicationLog** to assist you in debugging your macro.</span></span>

<span data-ttu-id="8da19-118">При использовании действия **LogEvent** для записи в таблицу **USysApplicationLog** для столбца **"Категория"** автоматически устанавливается **"Пользователь".**</span><span class="sxs-lookup"><span data-stu-id="8da19-118">When you use the **LogEvent** action to write to the **USysApplicationLog** table, the **Category** column is automatically set to **User**.</span></span>

<span data-ttu-id="8da19-119">Чтобы увидеть **таблицу USysApplicationLog,** с помощью следующих действий:</span><span class="sxs-lookup"><span data-stu-id="8da19-119">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="8da19-120">Щелкните **меню "Файл"** и выберите пункт **"Параметры".**</span><span class="sxs-lookup"><span data-stu-id="8da19-120">Click the **File** menu,and then click **Options**.</span></span>

2.  <span data-ttu-id="8da19-121">В **диалоговом окне** "Параметры access" перейдите на вкладку **"Текущая база данных".**</span><span class="sxs-lookup"><span data-stu-id="8da19-121">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="8da19-122">В разделе **"Навигация"** щелкните **"Параметры навигации".**</span><span class="sxs-lookup"><span data-stu-id="8da19-122">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="8da19-123">В **диалоговом окне "Параметры** навигации" щелкните **"Показать системные объекты"** и нажмите кнопку **"ОК".**</span><span class="sxs-lookup"><span data-stu-id="8da19-123">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="8da19-124">Нажмите **кнопку** "ОК", чтобы отклонять **диалоговое окно "Параметры** доступа".</span><span class="sxs-lookup"><span data-stu-id="8da19-124">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

