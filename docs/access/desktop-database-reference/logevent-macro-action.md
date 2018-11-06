---
title: Макрокоманда LogEvent
TOCTitle: LogEvent macro action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edc2fcaa72f6bfb912708948903aa09b25447580
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998176"
---
# <a name="logevent-macro-action"></a><span data-ttu-id="c7ee7-102">Макрокоманда LogEvent</span><span class="sxs-lookup"><span data-stu-id="c7ee7-102">LogEvent macro action</span></span>

<span data-ttu-id="c7ee7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c7ee7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c7ee7-104">Действие **LogEvent** записывает сведения об **системы см** .</span><span class="sxs-lookup"><span data-stu-id="c7ee7-104">The **LogEvent** action writes information to the **USysApplicationLog** system table.</span></span>

> [!NOTE]
> <span data-ttu-id="c7ee7-105">**LogEvent** действие доступно только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="c7ee7-105">The **LogEvent** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="c7ee7-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="c7ee7-106">Setting</span></span>

<span data-ttu-id="c7ee7-107">Действие **LogEvent** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="c7ee7-107">The **LogEvent** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7ee7-108">Argument</span><span class="sxs-lookup"><span data-stu-id="c7ee7-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="c7ee7-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c7ee7-109">Required</span></span></p></th>
<th><p><span data-ttu-id="c7ee7-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c7ee7-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7ee7-111"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="c7ee7-111"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="c7ee7-112">НЕТ</span><span class="sxs-lookup"><span data-stu-id="c7ee7-112">No</span></span></p></td>
<td><p><span data-ttu-id="c7ee7-113">Строковое выражение, описывающее условие, следует регистрировать.</span><span class="sxs-lookup"><span data-stu-id="c7ee7-113">A string expression that describes the condition that you want to log.</span></span> <span data-ttu-id="c7ee7-114">Описание не может превышать 255 знаков.</span><span class="sxs-lookup"><span data-stu-id="c7ee7-114">The description cannot exceed 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="c7ee7-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="c7ee7-115">Remarks</span></span>

<span data-ttu-id="c7ee7-116">Действие **LogEvent** можно использовать для записи сведений о состоянии **, не никак с помощью действия **[RaiseError](raiseerror-macro-action.md)** приводит к возникновению ошибки системы см** .</span><span class="sxs-lookup"><span data-stu-id="c7ee7-116">The **LogEvent** action can be used to write status information to the **USysApplicationLog** system table that does not merit using the **[RaiseError](raiseerror-macro-action.md)** action to throw an error.</span></span> <span data-ttu-id="c7ee7-117">К примеру вы журнал изменений для определенного поля или использовать при отладке макрос с помощью элементов в **USysApplicationLog** .</span><span class="sxs-lookup"><span data-stu-id="c7ee7-117">For example, you could log changes to a specific field, or use the items written to the **USysApplicationLog** to assist you in debugging your macro.</span></span>

<span data-ttu-id="c7ee7-118">При использовании **LogEvent** действие для записи **см** в столбце **категории** автоматически устанавливается значение **пользователя**.</span><span class="sxs-lookup"><span data-stu-id="c7ee7-118">When you use the **LogEvent** action to write to the **USysApplicationLog** table, the **Category** column is automatically set to **User**.</span></span>

<span data-ttu-id="c7ee7-119">Чтобы просмотреть **сведения см** , выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="c7ee7-119">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="c7ee7-120">Выберите в меню **файл** и выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="c7ee7-120">Click the **File** menu,and then click **Options**.</span></span>

2.  <span data-ttu-id="c7ee7-121">В диалоговом окне **Параметры доступа к** перейдите на вкладку **Текущей базы данных** .</span><span class="sxs-lookup"><span data-stu-id="c7ee7-121">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="c7ee7-122">В разделе **Переходы** щелкните **Параметры навигации**.</span><span class="sxs-lookup"><span data-stu-id="c7ee7-122">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="c7ee7-123">В диалоговом окне **Параметры навигации** нажмите кнопку **Показать системные объекты**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c7ee7-123">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="c7ee7-124">Нажмите **кнопку ОК** , чтобы закрыть диалоговое окно **Параметры доступа** .</span><span class="sxs-lookup"><span data-stu-id="c7ee7-124">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

