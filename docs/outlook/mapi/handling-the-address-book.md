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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413922"
---
# <a name="handling-the-address-book"></a><span data-ttu-id="95aff-103">Обработка адресной книги</span><span class="sxs-lookup"><span data-stu-id="95aff-103">Handling the address book</span></span>
  
<span data-ttu-id="95aff-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95aff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95aff-105">��������� �������� ����� MAPI ����� �������� ���������� ������ ��� ������������� � �������� ����������� ���������, ��������� ���������� ������� ������ ����������, ���������� ������������� ������ ����������� ����������� ��� ������ ��������, �������� one-offs � ����������� ���� ��� ��������� ���������������� ���������� ���� ����� ��������� ������������� ������������� �������� �� ������ � ������� ���������.</span><span class="sxs-lookup"><span data-stu-id="95aff-105">Handling the MAPI address book can include extracting entries to be used as message recipients, modifying recipient properties, adding messaging users or distribution lists, creating one-offs, and displaying one or more of the common address dialog boxes to allow users to browse address information and make changes.</span></span>

- <span data-ttu-id="95aff-106">[Открытие адресной книги](opening-the-address-book.md): описывается, как использовать MAPI для открытия адресной книги.</span><span class="sxs-lookup"><span data-stu-id="95aff-106">[Opening the Address Book](opening-the-address-book.md): Describes how to use MAPI to open an address book.</span></span>
    
- <span data-ttu-id="95aff-107">[Отображение диалоговых окна "Общий адрес":](displaying-the-common-address-dialog-box.md)описание отображения различных контейнеров адресной книги.</span><span class="sxs-lookup"><span data-stu-id="95aff-107">[Displaying the Common Address Dialog Box](displaying-the-common-address-dialog-box.md): Describes how to display different address book containers.</span></span>
    
- <span data-ttu-id="95aff-108">[Открытие контейнера адресной книги](opening-an-address-book-container.md): описывает открытие различных контейнеров адресной книги.</span><span class="sxs-lookup"><span data-stu-id="95aff-108">[Opening an Address Book Container](opening-an-address-book-container.md): Describes how to open different address book containers.</span></span>
    
- <span data-ttu-id="95aff-109">[Setting Address Book Options](setting-address-book-options.md): Describes how to set the properties that describe options for using the address book.</span><span class="sxs-lookup"><span data-stu-id="95aff-109">[Setting Address Book Options](setting-address-book-options.md): Describes how to set the properties that describe options for using the address book.</span></span>
    
- <span data-ttu-id="95aff-110">[Создание получателя](creating-a-recipient.md): описывается, как создавать получателей при обращении к сообщениям и добавлении записей в изменимые контейнеры адресной книги.</span><span class="sxs-lookup"><span data-stu-id="95aff-110">[Creating a Recipient](creating-a-recipient.md): Describes how to create recipients when addressing messages and adding entries to modifiable address book containers.</span></span>
    
- <span data-ttu-id="95aff-111">[Создание списка рассылки](creating-a-distribution-list.md): описывает создание списка рассылки в измояемом контейнере.</span><span class="sxs-lookup"><span data-stu-id="95aff-111">[Creating a Distribution List](creating-a-distribution-list.md): Describes how to create a distribution list into a modifiable container.</span></span>
    
- <span data-ttu-id="95aff-112">[Копирование получателя](copying-a-recipient.md): описывается копирование получателей из одного контейнера в другой или в тот же контейнер.</span><span class="sxs-lookup"><span data-stu-id="95aff-112">[Copying a Recipient](copying-a-recipient.md): Describes how to copy recipients from one container into another or the same container.</span></span>
    
- <span data-ttu-id="95aff-113">[Удаление получателя](deleting-a-recipient.md): описывается, как удалить одну или несколько записей адресной книги из измояемого контейнера.</span><span class="sxs-lookup"><span data-stu-id="95aff-113">[Deleting a Recipient](deleting-a-recipient.md): Describes how to remove one or more address book entries from a modifiable container.</span></span>
    
- <span data-ttu-id="95aff-114">[Подготовка получателя](preparing-a-recipient.md): описывается, как подготовить получателей путем преобразования их краткосрочных идентификаторов записей в долгосрочные идентификаторы записей и, возможно, добавления, изменения или изменения свойств.</span><span class="sxs-lookup"><span data-stu-id="95aff-114">[Preparing a Recipient](preparing-a-recipient.md): Describes how to prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span>
    
- <span data-ttu-id="95aff-115">[Доступ к участникам списка рассылки](accessing-the-members-of-a-distribution-list.md): описывает, как получить доступ к членам списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="95aff-115">[Accessing the Members of a Distribution List](accessing-the-members-of-a-distribution-list.md): Describes how to access the members of a distribution list.</span></span>
    
- <span data-ttu-id="95aff-116">[Искомые свойства получателя](retrieving-recipient-properties.md): описывается, как получить доступ к одному или несколько свойств записи адресной книги получателя.</span><span class="sxs-lookup"><span data-stu-id="95aff-116">[Retrieving Recipient Properties](retrieving-recipient-properties.md): Describes how to access one or more properties of a recipient address book entry.</span></span>
    
- <span data-ttu-id="95aff-117">[Поиск в адресной книге](searching-the-address-book.md): описывает два уровня функциональности поиска MAPI.</span><span class="sxs-lookup"><span data-stu-id="95aff-117">[Searching the Address Book](searching-the-address-book.md): Describes the two levels of MAPI search functionality.</span></span> 
    
- <span data-ttu-id="95aff-118">[Использование диалоговых окне "Расширенный поиск":](using-an-advanced-search-dialog-box.md)описание запуска расширенных функций поиска в контейнере адресной книги.</span><span class="sxs-lookup"><span data-stu-id="95aff-118">[Using an Advanced Search Dialog Box](using-an-advanced-search-dialog-box.md): Describes how to run an advanced search functionality in an address book container.</span></span>
    
- <span data-ttu-id="95aff-119">[Разрешение имени получателя](resolving-a-recipient-name.md): описывает, как разрешить имя в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="95aff-119">[Resolving a Recipient Name](resolving-a-recipient-name.md): Describes how to resolve a name in an address book.</span></span>
    
- <span data-ttu-id="95aff-120">[Expanding Distribution Lists](expanding-distribution-lists.md): Describes how to prompt MAPI to expand a distribution list.</span><span class="sxs-lookup"><span data-stu-id="95aff-120">[Expanding Distribution Lists](expanding-distribution-lists.md): Describes how to prompt MAPI to expand a distribution list.</span></span>
    

