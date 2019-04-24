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
# <a name="sendemail-macro-action"></a><span data-ttu-id="a07f6-102">Макрокоманда SendEmail</span><span class="sxs-lookup"><span data-stu-id="a07f6-102">SendEmail macro action</span></span>

<span data-ttu-id="a07f6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a07f6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a07f6-104">Действие **SendEmail** отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a07f6-104">The **SendEmail** action sends an email message.</span></span>

> [!NOTE]
> <span data-ttu-id="a07f6-105">Действие **SendEmail** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="a07f6-105">The **SendEmail** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="a07f6-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="a07f6-106">Setting</span></span>

<span data-ttu-id="a07f6-107">Макрокоманда **SendEmail** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="a07f6-107">The **SendEmail** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a07f6-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="a07f6-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="a07f6-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a07f6-109">Required</span></span></p></th>
<th><p><span data-ttu-id="a07f6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a07f6-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a07f6-111"><strong>To</strong></span><span class="sxs-lookup"><span data-stu-id="a07f6-111"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="a07f6-112">Да</span><span class="sxs-lookup"><span data-stu-id="a07f6-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="a07f6-113">Получатели сообщения, чьи имена вы хотите поместить в строку " <strong>Кому</strong> " в сообщении. РазДеляйте имена получателей, указанные в этом аргументе (а в аргументах <em>"копия"</em> и <em>"СК"</em> ), точкой с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="a07f6-113">The recipients of the message whose names you want to put on the <strong>To</strong> line in the message.Separate the recipient names that you specify in this argument (and in the <em>Cc</em> and <em>Bcc</em> arguments) with a semicolon (;).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a07f6-114"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="a07f6-114"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="a07f6-115">Нет</span><span class="sxs-lookup"><span data-stu-id="a07f6-115">No</span></span></p></td>
<td><p><span data-ttu-id="a07f6-116">Получатели сообщения, чьи имена вы хотите поместить в строку CC (&quot;копия&quot;) сообщения.</span><span class="sxs-lookup"><span data-stu-id="a07f6-116">The message recipients whose names you want to put on the Cc (&quot;carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a07f6-117"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="a07f6-117"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="a07f6-118">Нет</span><span class="sxs-lookup"><span data-stu-id="a07f6-118">No</span></span></p></td>
<td><p><span data-ttu-id="a07f6-119">Получатели сообщения, имена которых необходимо поместить в строку "СК" (&quot;Скрытая копия&quot;) в сообщении.</span><span class="sxs-lookup"><span data-stu-id="a07f6-119">The message recipients whose names you want to put on the Bcc (&quot;blind carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a07f6-120"><strong>Subject</strong></span><span class="sxs-lookup"><span data-stu-id="a07f6-120"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="a07f6-121">Нет</span><span class="sxs-lookup"><span data-stu-id="a07f6-121">No</span></span></p></td>
<td><p><span data-ttu-id="a07f6-122">Тема сообщения.</span><span class="sxs-lookup"><span data-stu-id="a07f6-122">The subject of the message.</span></span> <span data-ttu-id="a07f6-123">Этот текст отображается в строке <strong>темы</strong> сообщения.</span><span class="sxs-lookup"><span data-stu-id="a07f6-123">This text appears on the <strong>Subject</strong> line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a07f6-124"><strong>Body</strong></span><span class="sxs-lookup"><span data-stu-id="a07f6-124"><strong>Body</strong></span></span></p></td>
<td><p><span data-ttu-id="a07f6-125">Нет</span><span class="sxs-lookup"><span data-stu-id="a07f6-125">No</span></span></p></td>
<td><p><span data-ttu-id="a07f6-126">Текст, который необходимо включить в основной текст почтового сообщения.</span><span class="sxs-lookup"><span data-stu-id="a07f6-126">The text that you want to include in the main body of the mail message.</span></span> <span data-ttu-id="a07f6-127">Если оставить этот аргумент пустым, в сообщение не будет добавлен никакой дополнительный текст.</span><span class="sxs-lookup"><span data-stu-id="a07f6-127">If you leave this argument blank, no additional text is included in the message.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a07f6-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="a07f6-128">Remarks</span></span>

<span data-ttu-id="a07f6-129">Действие **SendEmail** доступно только в макросах **[после удаления](after-delete-macro-event.md)**, **[после вставки](after-insert-macro-event.md)** и **[после обновления](after-update-macro-event.md)** событий макросов.</span><span class="sxs-lookup"><span data-stu-id="a07f6-129">The **SendEmail** action is available only in the **[After Delete](after-delete-macro-event.md)**, **[After Insert](after-insert-macro-event.md)**, and **[After Update](after-update-macro-event.md)** macro events.</span></span>

<span data-ttu-id="a07f6-130">Действие **SendEmail** не отображает сообщение для редактирования.</span><span class="sxs-lookup"><span data-stu-id="a07f6-130">The **SendEmail** action does not display the message for editing.</span></span>

