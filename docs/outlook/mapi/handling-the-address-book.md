---
title: Обработка адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b685244a-fe1b-4416-85d3-4bd86ccbc3aa
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 464549732562a4a02d081dc5a4c5e573e38cbbce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299421"
---
# <a name="handling-the-address-book"></a><span data-ttu-id="c868d-103">Обработка адресной книги</span><span class="sxs-lookup"><span data-stu-id="c868d-103">Handling the address book</span></span>
  
<span data-ttu-id="c868d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c868d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c868d-105">��������� �������� ����� MAPI ����� �������� ���������� ������ ��� ������������� � �������� ����������� ���������, ��������� ���������� ������� ������ ����������, ���������� ������������� ������ ����������� ����������� ��� ������ ��������, �������� one-offs � ����������� ���� ��� ��������� ���������������� ���������� ���� ����� ��������� ������������� ������������� �������� �� ������ � ������� ���������.</span><span class="sxs-lookup"><span data-stu-id="c868d-105">Handling the MAPI address book can include extracting entries to be used as message recipients, modifying recipient properties, adding messaging users or distribution lists, creating one-offs, and displaying one or more of the common address dialog boxes to allow users to browse address information and make changes.</span></span>

- <span data-ttu-id="c868d-106">[Открытие адресной книги](opening-the-address-book.md): в этой статье описано, как с помощью интерфейса MAPI открыть адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="c868d-106">[Opening the Address Book](opening-the-address-book.md): Describes how to use MAPI to open an address book.</span></span>
    
- <span data-ttu-id="c868d-107">[Отображение диалогОвого окна "общий адрес"](displaying-the-common-address-dialog-box.md): сведения о том, как отображать различные контейнеры адресных книг.</span><span class="sxs-lookup"><span data-stu-id="c868d-107">[Displaying the Common Address Dialog Box](displaying-the-common-address-dialog-box.md): Describes how to display different address book containers.</span></span>
    
- <span data-ttu-id="c868d-108">[Открытие контейнера адресной книги](opening-an-address-book-container.md): Описание открытия различных контейнеров адресных книг.</span><span class="sxs-lookup"><span data-stu-id="c868d-108">[Opening an Address Book Container](opening-an-address-book-container.md): Describes how to open different address book containers.</span></span>
    
- <span data-ttu-id="c868d-109">[Настройка параметров адресной книги](setting-address-book-options.md): в этой статье описывается, как задать свойства, описывающие параметры использования адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c868d-109">[Setting Address Book Options](setting-address-book-options.md): Describes how to set the properties that describe options for using the address book.</span></span>
    
- <span data-ttu-id="c868d-110">[Создание получателя](creating-a-recipient.md): в этой статье описано, как создавать получателей при адресации сообщений и добавлении записей в изменяемые контейнеры адресных книг.</span><span class="sxs-lookup"><span data-stu-id="c868d-110">[Creating a Recipient](creating-a-recipient.md): Describes how to create recipients when addressing messages and adding entries to modifiable address book containers.</span></span>
    
- <span data-ttu-id="c868d-111">[Создание списка рассылки](creating-a-distribution-list.md): в этой статье описано, как создать список рассылки в изменяемом контейнере.</span><span class="sxs-lookup"><span data-stu-id="c868d-111">[Creating a Distribution List](creating-a-distribution-list.md): Describes how to create a distribution list into a modifiable container.</span></span>
    
- <span data-ttu-id="c868d-112">[Копирование получателя](copying-a-recipient.md): в этой статье описано, как копировать получателей из одного контейнера в другой или один контейнер.</span><span class="sxs-lookup"><span data-stu-id="c868d-112">[Copying a Recipient](copying-a-recipient.md): Describes how to copy recipients from one container into another or the same container.</span></span>
    
- <span data-ttu-id="c868d-113">[Удаление получателя](deleting-a-recipient.md): в этой статье описано, как удалить одну или несколько записей адресной книги из изменяемого контейнера.</span><span class="sxs-lookup"><span data-stu-id="c868d-113">[Deleting a Recipient](deleting-a-recipient.md): Describes how to remove one or more address book entries from a modifiable container.</span></span>
    
- <span data-ttu-id="c868d-114">[Подготовка получателя](preparing-a-recipient.md): в этой статье описано, как подготовить получателей путем преобразования краткосрочных идентификаторов записей в долгосрочные идентификаторы записей и, возможно, для добавления, изменения или изменения порядка свойств.</span><span class="sxs-lookup"><span data-stu-id="c868d-114">[Preparing a Recipient](preparing-a-recipient.md): Describes how to prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span>
    
- <span data-ttu-id="c868d-115">[Доступ к участникам списка рассылки](accessing-the-members-of-a-distribution-list.md): в этой статье описывается, как получить доступ к участникам списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="c868d-115">[Accessing the Members of a Distribution List](accessing-the-members-of-a-distribution-list.md): Describes how to access the members of a distribution list.</span></span>
    
- <span data-ttu-id="c868d-116">[Получение свойств получателя](retrieving-recipient-properties.md): в этой статье описывается, как получить доступ к одному или нескольким свойствам записи адресной книги получателя.</span><span class="sxs-lookup"><span data-stu-id="c868d-116">[Retrieving Recipient Properties](retrieving-recipient-properties.md): Describes how to access one or more properties of a recipient address book entry.</span></span>
    
- <span data-ttu-id="c868d-117">[Поиск в адресной книге](searching-the-address-book.md): описание двух уровней функций поиска MAPI.</span><span class="sxs-lookup"><span data-stu-id="c868d-117">[Searching the Address Book](searching-the-address-book.md): Describes the two levels of MAPI search functionality.</span></span> 
    
- <span data-ttu-id="c868d-118">[Использование диалогОвого окна "Расширенный Поиск"](using-an-advanced-search-dialog-box.md): инструкции по запуску расширенных функций поиска в контейнере адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c868d-118">[Using an Advanced Search Dialog Box](using-an-advanced-search-dialog-box.md): Describes how to run an advanced search functionality in an address book container.</span></span>
    
- <span data-ttu-id="c868d-119">[Разрешение имени получателя](resolving-a-recipient-name.md): в этой статье описывается, как разрешить имя в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="c868d-119">[Resolving a Recipient Name](resolving-a-recipient-name.md): Describes how to resolve a name in an address book.</span></span>
    
- <span data-ttu-id="c868d-120">[Развертывание списков рассылки](expanding-distribution-lists.md): в этой статье описывается, как запрашивать MAPI для расширения списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="c868d-120">[Expanding Distribution Lists](expanding-distribution-lists.md): Describes how to prompt MAPI to expand a distribution list.</span></span>
    

