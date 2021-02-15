---
title: Макрокоманда SendEmail
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c0fa220b3088cde46b0e82631c06520afd839c64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314653"
---
# <a name="sendemail-macro-action"></a><span data-ttu-id="219c2-102">Макрокоманда SendEmail</span><span class="sxs-lookup"><span data-stu-id="219c2-102">SendEmail macro action</span></span>

<span data-ttu-id="219c2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="219c2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="219c2-104">Действие **SendEmail** отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="219c2-104">The **SendEmail** action sends an email message.</span></span>

> [!NOTE]
> <span data-ttu-id="219c2-105">Действие **SendEmail** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="219c2-105">The **SendEmail** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="219c2-106">Setting</span><span class="sxs-lookup"><span data-stu-id="219c2-106">Setting</span></span>

<span data-ttu-id="219c2-107">Действие **SendEmail** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="219c2-107">The **SendEmail** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="219c2-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="219c2-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="219c2-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="219c2-109">Required</span></span></p></th>
<th><p><span data-ttu-id="219c2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="219c2-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="219c2-111"><strong>Для</strong></span><span class="sxs-lookup"><span data-stu-id="219c2-111"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="219c2-112">Да</span><span class="sxs-lookup"><span data-stu-id="219c2-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="219c2-113">Получатели сообщения, имена которых нужно поместить в строку <strong>"Кому"</strong> в сообщении. Разделять имена получателей, задамые в <em></em> этом аргументе (и в аргументах <em>"Ск"</em> и "СК"), с заданной заданной четной точкаю (;).</span><span class="sxs-lookup"><span data-stu-id="219c2-113">The recipients of the message whose names you want to put on the <strong>To</strong> line in the message.Separate the recipient names that you specify in this argument (and in the <em>Cc</em> and <em>Bcc</em> arguments) with a semicolon (;).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="219c2-114"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="219c2-114"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="219c2-115">Нет</span><span class="sxs-lookup"><span data-stu-id="219c2-115">No</span></span></p></td>
<td><p><span data-ttu-id="219c2-116">Получатели сообщений, имена которых нужно поместить в строку &quot; "Копия" (копия) &quot; сообщения.</span><span class="sxs-lookup"><span data-stu-id="219c2-116">The message recipients whose names you want to put on the Cc (&quot;carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="219c2-117"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="219c2-117"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="219c2-118">Нет</span><span class="sxs-lookup"><span data-stu-id="219c2-118">No</span></span></p></td>
<td><p><span data-ttu-id="219c2-119">Получатели сообщений, имена которых нужно поместить в строку "СК" &quot; (жалюзийная &quot; копия) сообщения.</span><span class="sxs-lookup"><span data-stu-id="219c2-119">The message recipients whose names you want to put on the Bcc (&quot;blind carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="219c2-120"><strong>Тема</strong></span><span class="sxs-lookup"><span data-stu-id="219c2-120"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="219c2-121">Нет</span><span class="sxs-lookup"><span data-stu-id="219c2-121">No</span></span></p></td>
<td><p><span data-ttu-id="219c2-122">Тема сообщения.</span><span class="sxs-lookup"><span data-stu-id="219c2-122">The subject of the message.</span></span> <span data-ttu-id="219c2-123">Этот текст отображается в <strong>строке темы</strong> сообщения.</span><span class="sxs-lookup"><span data-stu-id="219c2-123">This text appears on the <strong>Subject</strong> line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="219c2-124"><strong>Основной текст</strong></span><span class="sxs-lookup"><span data-stu-id="219c2-124"><strong>Body</strong></span></span></p></td>
<td><p><span data-ttu-id="219c2-125">Нет</span><span class="sxs-lookup"><span data-stu-id="219c2-125">No</span></span></p></td>
<td><p><span data-ttu-id="219c2-126">Текст, который вы хотите включить в основной текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="219c2-126">The text that you want to include in the main body of the mail message.</span></span> <span data-ttu-id="219c2-127">Если оставить этот аргумент пустым, в сообщение не будет включен дополнительный текст.</span><span class="sxs-lookup"><span data-stu-id="219c2-127">If you leave this argument blank, no additional text is included in the message.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="219c2-128">Заметки</span><span class="sxs-lookup"><span data-stu-id="219c2-128">Remarks</span></span>

<span data-ttu-id="219c2-129">Действие **SendEmail** доступно только в событиях макроса **["После удаления",](after-delete-macro-event.md)** **["После вставки"](after-insert-macro-event.md)** и **["После обновления".](after-update-macro-event.md)**</span><span class="sxs-lookup"><span data-stu-id="219c2-129">The **SendEmail** action is available only in the **[After Delete](after-delete-macro-event.md)**, **[After Insert](after-insert-macro-event.md)**, and **[After Update](after-update-macro-event.md)** macro events.</span></span>

<span data-ttu-id="219c2-130">Действие **SendEmail** не отображает сообщение для редактирования.</span><span class="sxs-lookup"><span data-stu-id="219c2-130">The **SendEmail** action does not display the message for editing.</span></span>

