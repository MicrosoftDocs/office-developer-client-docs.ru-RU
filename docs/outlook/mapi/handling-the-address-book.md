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
ms.openlocfilehash: 7a72d0e90e6c28874f341fc9ba7af843a44c5da8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583325"
---
# <a name="handling-the-address-book"></a><span data-ttu-id="83cde-103">Обработка адресной книги</span><span class="sxs-lookup"><span data-stu-id="83cde-103">Handling the address book</span></span>
  
<span data-ttu-id="83cde-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83cde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83cde-105">��������� �������� ����� MAPI ����� �������� ���������� ������ ��� ������������� � �������� ����������� ���������, ��������� ���������� ������� ������ ����������, ���������� ������������� ������ ����������� ����������� ��� ������ ��������, �������� one-offs � ����������� ���� ��� ��������� ���������������� ���������� ���� ����� ��������� ������������� ������������� �������� �� ������ � ������� ���������.</span><span class="sxs-lookup"><span data-stu-id="83cde-105">Handling the MAPI address book can include extracting entries to be used as message recipients, modifying recipient properties, adding messaging users or distribution lists, creating one-offs, and displaying one or more of the common address dialog boxes to allow users to browse address information and make changes.</span></span>

- <span data-ttu-id="83cde-106">[Открытие адресной книги](opening-the-address-book.md): описывается, как использовать MAPI, чтобы открыть адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="83cde-106">[Opening the Address Book](opening-the-address-book.md): Describes how to use MAPI to open an address book.</span></span>
    
- <span data-ttu-id="83cde-107">[Отображение стандартным диалоговым окном адрес](displaying-the-common-address-dialog-box.md): Описание способов отображения различных адресной книги контейнеров.</span><span class="sxs-lookup"><span data-stu-id="83cde-107">[Displaying the Common Address Dialog Box](displaying-the-common-address-dialog-box.md): Describes how to display different address book containers.</span></span>
    
- <span data-ttu-id="83cde-108">[Открытие контейнер адресной книги](opening-an-address-book-container.md): описывается, как открыть контейнеров различных адресной книги.</span><span class="sxs-lookup"><span data-stu-id="83cde-108">[Opening an Address Book Container](opening-an-address-book-container.md): Describes how to open different address book containers.</span></span>
    
- <span data-ttu-id="83cde-109">[Параметр параметры адресной книги](setting-address-book-options.md): описывается, как задать свойства, описывающие параметры для использования в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="83cde-109">[Setting Address Book Options](setting-address-book-options.md): Describes how to set the properties that describe options for using the address book.</span></span>
    
- <span data-ttu-id="83cde-110">[Создание получателя](creating-a-recipient.md): описывает порядок создания получатели при отправке сообщений и добавление записей в контейнеров изменяемые адресной книги.</span><span class="sxs-lookup"><span data-stu-id="83cde-110">[Creating a Recipient](creating-a-recipient.md): Describes how to create recipients when addressing messages and adding entries to modifiable address book containers.</span></span>
    
- <span data-ttu-id="83cde-111">[Создание списка рассылки](creating-a-distribution-list.md): описывается, как создать список рассылки, в контейнере можно изменить.</span><span class="sxs-lookup"><span data-stu-id="83cde-111">[Creating a Distribution List](creating-a-distribution-list.md): Describes how to create a distribution list into a modifiable container.</span></span>
    
- <span data-ttu-id="83cde-112">[Копирование получателя](copying-a-recipient.md): Описание копирования получателей из одного контейнера в другой или же контейнера.</span><span class="sxs-lookup"><span data-stu-id="83cde-112">[Copying a Recipient](copying-a-recipient.md): Describes how to copy recipients from one container into another or the same container.</span></span>
    
- <span data-ttu-id="83cde-113">[Удаление получателя](deleting-a-recipient.md): Описание удаления одного или нескольких записей адресной книги из изменяемые контейнера.</span><span class="sxs-lookup"><span data-stu-id="83cde-113">[Deleting a Recipient](deleting-a-recipient.md): Describes how to remove one or more address book entries from a modifiable container.</span></span>
    
- <span data-ttu-id="83cde-114">[Подготовка получателя](preparing-a-recipient.md): описание подготавливает получателей, преобразование их краткосрочных идентификаторы записей для долгосрочного идентификаторы записей и возможно добавления, изменения или изменение порядка свойств.</span><span class="sxs-lookup"><span data-stu-id="83cde-114">[Preparing a Recipient](preparing-a-recipient.md): Describes how to prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span>
    
- <span data-ttu-id="83cde-115">[Доступ к членам списка рассылки](accessing-the-members-of-a-distribution-list.md): Описание способов доступа к элементам списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="83cde-115">[Accessing the Members of a Distribution List](accessing-the-members-of-a-distribution-list.md): Describes how to access the members of a distribution list.</span></span>
    
- <span data-ttu-id="83cde-116">[Извлечение свойств получателя](retrieving-recipient-properties.md): Описание способов доступа к одного или нескольких свойств записи получателей адресной книги.</span><span class="sxs-lookup"><span data-stu-id="83cde-116">[Retrieving Recipient Properties](retrieving-recipient-properties.md): Describes how to access one or more properties of a recipient address book entry.</span></span>
    
- <span data-ttu-id="83cde-117">[Поиск в адресной книге](searching-the-address-book.md): описание двух уровней функций поиска MAPI.</span><span class="sxs-lookup"><span data-stu-id="83cde-117">[Searching the Address Book](searching-the-address-book.md): Describes the two levels of MAPI search functionality.</span></span> 
    
- <span data-ttu-id="83cde-118">[С помощью расширенных диалоговое окно поиска](using-an-advanced-search-dialog-box.md): описывается, как запустить расширенный поиск функциональность в контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="83cde-118">[Using an Advanced Search Dialog Box](using-an-advanced-search-dialog-box.md): Describes how to run an advanced search functionality in an address book container.</span></span>
    
- <span data-ttu-id="83cde-119">[Разрешения имени получателя](resolving-a-recipient-name.md): Описание способов разрешения имени в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="83cde-119">[Resolving a Recipient Name](resolving-a-recipient-name.md): Describes how to resolve a name in an address book.</span></span>
    
- <span data-ttu-id="83cde-120">[Расширение списка рассылки](expanding-distribution-lists.md): описывается, как запрашивать MAPI разверните список рассылки.</span><span class="sxs-lookup"><span data-stu-id="83cde-120">[Expanding Distribution Lists](expanding-distribution-lists.md): Describes how to prompt MAPI to expand a distribution list.</span></span>
    

