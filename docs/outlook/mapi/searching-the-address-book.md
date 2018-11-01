---
title: Поиск по адресной книге
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20ff2b63-e4a3-4ba9-bad0-2c1873fb69b5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0d3fb5d2ce5036c6491e24bba8d3541b123eaab1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595127"
---
# <a name="searching-the-address-book"></a>Поиск по адресной книге

**Область применения**: Outlook 2013 | Outlook 2016 
  
MAPI ��������� ������������ �������� ����� ��� ���������� ���� ������� ������� ������:
  
- Базовый уровень, совпадают с указанным с помощью свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) записей адресной книги. ���� ������� ��������� �������������, ��������, ��� ��������� ������� �������� �, �������� ������� ���������� � ������-����� � ������� ���������� �������������� ������ ����������� �����������, ������� � ������.
    
- ������� �������������, ������� ������������� �� �������� �� **PR_DISPLAY_NAME**. ���� ������� ��������� �������������, ��������, ��� ���������� �� ������ � ����� ������� ������ ����������� � ������ ����� � ����� ����������� ������ �������������.
    
Because address book providers can support searching for each of their containers at the basic level, at both levels, or choose not to support it at all, do not expect searching to be implemented as a standard feature. To determine if a particular container supports searches, attempt to establish search criteria in a call to its [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. If **SetSearchCriteria** returns MAPI_E_NO_SUPPORT, the container does not support searches. 
  
In a container that supports searches, retrieve established criteria by calling [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md). You can also request that the user be prompted for search criteria before a container's contents table is displayed. Чтобы выбрать этот параметр, задайте флаг AB_FIND_ON_OPEN свойства **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) контейнера. After the user enters the criteria, it is stored as a restriction and passed to the **SetSearchCriteria** method. Setting AB_FIND_ON_OPEN is particularly useful if you are using an online service or any address book provider that has a slow link to its data. 
  
### <a name="to-perform-a-basic-search-in-an-address-book-container"></a>��� ���������� �������� ������ � ��������� �������� �����
  
1. Call the container's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table. 
    
2. �������� ������ ������, ������� ������������� ������������. ��������� ���������:
    
   - [IMAPITable::FindRow](imapitable-findrow.md) to locate a specific row in the table. 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md) to order rows in the table. 
    
   - [IMAPITable::Restrict](imapitable-restrict.md) to limit the table view. 
    
   - Ограничение свойства с помощью свойства **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) для разрешения неоднозначных имен. �������� **IMAPITable::Restrict**, ����� ��������� ��� �����������. 
    
   - [IABContainer::ResolveNames](iabcontainer-resolvenames.md) to resolve ambiguous names. 
    
3. Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve any rows that meet your applied search criteria. **QueryRows** can return zero or more matching rows. 
    
������ **FindRow**, **SortTable**� **Restrict** � ��� ������� ������, ��������� ��� ����� �������, ����� ���� �������, ������� ��� ���������� �����. **Связей с Общественностью\_ANR** ограничение свойство и метод **IABContainer::ResolveNames** относятся к поставщиками адресной книги и используется для разрешения неоднозначных имен. ������������� �����, ������ � ������ �����������, ������� �� ����� **PR_ENTRYID** ��������, ��������� � ����. 
  
**Связей с Общественностью\_ANR** ограничение вызывает алгоритм, который разделяет строку знаков на слова и сопоставляет эти слова со сведениями в адресной книге с помощью проверки префикса. The information used for the matching depends on the address book provider. All address book providers are required to support the **PR_ANR** restriction for their address book containers. For more information, see [���������� ���������� ����](implementing-name-resolution.md).
  
**IABContainer::ResolveNames** ��������� ����������� **PR_ANR** ��������� �� ��������� ���� ��� ������������� ��������� ������� ����������� ���������� ������ ���� �������. Вызов **ResolveNames** один раз для разрешения имен нескольких может быть намного быстрее, чем вызов **связей с Общественностью\_ANR** ограничение несколько раз. ��� �� ����� ������������ �������� ����� �� ��������� ��� ��������� **ResolveNames**.
  

