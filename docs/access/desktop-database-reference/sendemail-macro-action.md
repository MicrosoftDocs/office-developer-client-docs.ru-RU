---
title: Действия макроса sendemail действие
TOCTitle: SendEmail Macro Action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb2624a00ed2fdbe4a2b24a1f052e19217a4c1a9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871943"
---
# <a name="sendemail-macro-action"></a><span data-ttu-id="5d898-102">Действия макроса sendemail действие</span><span class="sxs-lookup"><span data-stu-id="5d898-102">SendEmail Macro Action</span></span>


<span data-ttu-id="5d898-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d898-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d898-104">Действие **sendemail действие** отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5d898-104">The **SendEmail** action sends an e-mail message.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5d898-105">Действие <STRONG>sendemail действие</STRONG> доступно только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="5d898-105">The <STRONG>SendEmail</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="5d898-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="5d898-106">Setting</span></span>

<span data-ttu-id="5d898-107">Действие **sendemail действие** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="5d898-107">The **SendEmail** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d898-108">Argument</span><span class="sxs-lookup"><span data-stu-id="5d898-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="5d898-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5d898-109">Required</span></span></p></th>
<th><p><span data-ttu-id="5d898-110">Описание</span><span class="sxs-lookup"><span data-stu-id="5d898-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d898-111"><strong>Задача</strong></span><span class="sxs-lookup"><span data-stu-id="5d898-111"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="5d898-112">Да</span><span class="sxs-lookup"><span data-stu-id="5d898-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="5d898-113">Получатели сообщения, имена которых требуется включить в строке <strong>Кому</strong> в сообщении. Разделите имена получателей, которые задают этот аргумент (и аргументы <em>«копия»</em> и <em>«СК»</em> ) точкой с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="5d898-113">The recipients of the message whose names you want to put on the <strong>To</strong> line in the message.Separate the recipient names that you specify in this argument (and in the <em>Cc</em> and <em>Bcc</em> arguments) with a semicolon (;).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d898-114"><strong>«Копия»</strong></span><span class="sxs-lookup"><span data-stu-id="5d898-114"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="5d898-115">Нет</span><span class="sxs-lookup"><span data-stu-id="5d898-115">No</span></span></p></td>
<td><p><span data-ttu-id="5d898-116">Получатели сообщения, имена которых следует разместить на «копия» (&quot;копии&quot;) в строке сообщения.</span><span class="sxs-lookup"><span data-stu-id="5d898-116">The message recipients whose names you want to put on the Cc (&quot;carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d898-117"><strong>Скрытой копии</strong></span><span class="sxs-lookup"><span data-stu-id="5d898-117"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="5d898-118">Нет</span><span class="sxs-lookup"><span data-stu-id="5d898-118">No</span></span></p></td>
<td><p><span data-ttu-id="5d898-119">Получатели сообщения, имена которых требуется включить в скрытой копии (&quot;скрытой копии&quot;) в строке сообщения.</span><span class="sxs-lookup"><span data-stu-id="5d898-119">The message recipients whose names you want to put on the Bcc (&quot;blind carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d898-120"><strong>Subject</strong></span><span class="sxs-lookup"><span data-stu-id="5d898-120"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="5d898-121">Нет</span><span class="sxs-lookup"><span data-stu-id="5d898-121">No</span></span></p></td>
<td><p><span data-ttu-id="5d898-122">Тема сообщения.</span><span class="sxs-lookup"><span data-stu-id="5d898-122">The subject of the message.</span></span> <span data-ttu-id="5d898-123">Этот текст отображается в строке <strong>темы</strong> сообщения.</span><span class="sxs-lookup"><span data-stu-id="5d898-123">This text appears on the <strong>Subject</strong> line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d898-124"><strong>Body</strong></span><span class="sxs-lookup"><span data-stu-id="5d898-124"><strong>Body</strong></span></span></p></td>
<td><p><span data-ttu-id="5d898-125">Нет</span><span class="sxs-lookup"><span data-stu-id="5d898-125">No</span></span></p></td>
<td><p><span data-ttu-id="5d898-126">Текст, который требуется включить в основном тексте сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5d898-126">The text that you want to include in the main body of the mail message.</span></span> <span data-ttu-id="5d898-127">Если оставить это аргумент, никакой текст включается в сообщении.</span><span class="sxs-lookup"><span data-stu-id="5d898-127">If you leave this argument blank, no additional text is included in the message.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5d898-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="5d898-128">Remarks</span></span>

<span data-ttu-id="5d898-129">**Sendemail действие** действие доступно только в **[После удаления](after-delete-macro-event.md)**, **[После вставки](after-insert-macro-event.md)** и события макрос **[После обновления](after-update-macro-event.md)** .</span><span class="sxs-lookup"><span data-stu-id="5d898-129">The **SendEmail** action is available only in the **[After Delete](after-delete-macro-event.md)**, **[After Insert](after-insert-macro-event.md)**, and **[After Update](after-update-macro-event.md)** macro events.</span></span>

<span data-ttu-id="5d898-130">Действие **sendemail действие** не отображает сообщение для редактирования.</span><span class="sxs-lookup"><span data-stu-id="5d898-130">The **SendEmail** action does not display the message for editing.</span></span>

