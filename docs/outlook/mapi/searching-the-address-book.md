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
ms.openlocfilehash: d40419291f4b09c5880a769ce231015511e8f269
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339741"
---
# <a name="searching-the-address-book"></a>Поиск по адресной книге

**Область применения**: Outlook 2013 | Outlook 2016 
  
MAPI ��������� ������������ �������� ����� ��� ���������� ���� ������� ������� ������:
  
- Базовый уровень, который соответствует заданному имени с помощью свойства **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) записей адресной книги. ���� ������� ��������� �������������, ��������, ��� ��������� ������� �������� �, �������� ������� ���������� � ������-����� � ������� ���������� �������������� ������ ����������� �����������, ������� � ������.
    
- ������� �������������, ������� ������������� �� �������� �� **PR_DISPLAY_NAME**. ���� ������� ��������� �������������, ��������, ��� ���������� �� ������ � ����� ������� ������ ����������� � ������ ����� � ����� ����������� ������ �������������.
    
Because address book providers can support searching for each of their containers at the basic level, at both levels, or choose not to support it at all, do not expect searching to be implemented as a standard feature. To determine if a particular container supports searches, attempt to establish search criteria in a call to its [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. If **SetSearchCriteria** returns MAPI_E_NO_SUPPORT, the container does not support searches. 
  
In a container that supports searches, retrieve established criteria by calling [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md). You can also request that the user be prompted for search criteria before a container's contents table is displayed. Чтобы выбрать этот параметр, установите флаг АБ_ФИНД_ОН_ОПЕН для свойства контейнера **пр_контаинер_флагс** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)). After the user enters the criteria, it is stored as a restriction and passed to the **SetSearchCriteria** method. Setting AB_FIND_ON_OPEN is particularly useful if you are using an online service or any address book provider that has a slow link to its data. 
  
### <a name="to-perform-a-basic-search-in-an-address-book-container"></a>��� ���������� �������� ������ � ��������� �������� �����
  
1. Call the container's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table. 
    
2. �������� ������ ������, ������� ������������� ������������. ��������� ���������:
    
   - [IMAPITable::FindRow](imapitable-findrow.md) to locate a specific row in the table. 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md) to order rows in the table. 
    
   - [IMAPITable::Restrict](imapitable-restrict.md) to limit the table view. 
    
   - Ограничение свойства с помощью свойства **пр_анр** ([PidTagAnr](pidtaganr-canonical-property.md)) для разрешения неоднозначных имен. �������� **IMAPITable::Restrict**, ����� ��������� ��� �����������. 
    
   - [IABContainer::ResolveNames](iabcontainer-resolvenames.md) to resolve ambiguous names. 
    
3. Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve any rows that meet your applied search criteria. **QueryRows** can return zero or more matching rows. 
    
������ **FindRow**, **SortTable**� **Restrict** � ��� ������� ������, ��������� ��� ����� �������, ����� ���� �������, ������� ��� ���������� �����. Метод restriction свойства **\_ANR** и метод **иабконтаинер:: ResolveNames** относятся к поставщикам адресных книг и используются для разрешения неоднозначных имен. ������������� �����, ������ � ������ �����������, ������� �� ����� **PR_ENTRYID** ��������, ��������� � ����. 
  
Ограничение **\_ANR** по методу ANR вызывает алгоритм, который отделяет строку символов на словах и сопоставляет эти слова со сведениями в адресной книге с использованием соответствия префиксу. The information used for the matching depends on the address book provider. All address book providers are required to support the **PR_ANR** restriction for their address book containers. For more information, see [���������� ���������� ����](implementing-name-resolution.md).
  
**IABContainer::ResolveNames** ��������� ����������� **PR_ANR** ��������� �� ��������� ���� ��� ������������� ��������� ������� ����������� ���������� ������ ���� �������. Вызов **ResolveNames** один раз для разрешения нескольких имен может выполняться гораздо быстрее, чем ограничение **на\_** разрешение до неоднократного вызова. ��� �� ����� ������������ �������� ����� �� ��������� ��� ��������� **ResolveNames**.
  

