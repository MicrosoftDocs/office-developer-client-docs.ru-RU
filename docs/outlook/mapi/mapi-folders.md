---
title: ����� MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8fac3c92-d2f5-479e-a368-ca82bddd8e30
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 88ddfd9e6bb27abfeee9750c71e98d4fad9d1a14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809741"
---
# <a name="mapi-folders"></a>����� MAPI

  
  
**Относится к**: Outlook 
  
����� � ��� ������� MAPI, ������� ������������ � �������� ��������� ����� ����������� ��� ���������. ������������ ������������ ����� ����� ��������� ��������� � ������ �����. ����� ��������� ��� ����������� � ������ � �����������.
  
����� ����������� ��������� [IMAPIFolder](imapifolderimapicontainer.md) , ������� �������� ����������� �� ���������� **IUnknown** ����� [IMAPIContainer](imapicontainerimapiprop.md) � [IMAPIProp](imapipropiunknown.md) ����������. ������� ���������� **IMAPIFolder** ��������, ����������� � �������� ��������� � �����, ����� �������� � ������ ��������� ��������� ��� ���������� ��� ������� ������ ������ ���� ��� ���������. �������� �� ��, ��� ����������� ��������� ��������� ���������� ��� ��������� ��� ������ � **IMAPIFolder**, ��������� ������ ������������� ������� ���������, ����� ������������� �������� ����������� ��������� ���������. MAPI ��������� ������������ �������� ����������� ��������� ��������� ��� ������ ��������� ����� ������� ������� ����� � ���������� [IMAPISupport](imapisupportiunknown.md) . ��������, ������ ���� ����� ������������� ����������� ������ ����������� ����������� ��������� ��������� ����� ������� ������ ����������� � ������� ��������� � �������� �� �� ����������. 
  
���������� ��� ���� �����.
  
- �������� �����.
    
- ������������� �����.
    
- ����� ������
    
������ ��������� ��������� ����� �� ������� ���� � �������� �����. � �������� ����� ������������ � ������� ����� �������� � �������� ��������� � ������ �����. �������� ����� �� ������� ���������, �����������, ������������� ��� ������. ���������� ������ ���� �������� ����� ��� ������� ��������� ���������.
  
����������� ����� � �������������. ��� � �������� ����� ������������� ����� �������� ��������� � ������ �����. � ������� �� �������� ����� �� ����� ����������, ����������, ������������� � �������. ������������� ����� ����� ���� ������� � �������� ����� ��� ������ ������������� �����. ����� ������ ������� ����� ����� � ������ �����, ����� ����� ���������� ��������� ����� ��� ��������� �����. �����, � ������� ����������� ����� ����� ���������� ������������ ����� ����� �����. ������������� �����, ������� ����� ���� � �� �� ����� ������������� ���������� �����. ������������� ������� � ��-����� ����� ��� ����� ����� ���������� �����, � ����������� �� ��������� ��������� ���������. ���������� ��������� ���������, ������� ������� ����� ��� �������� �������� ������ MAPI_E_COLLISION ��� ������� ������� ������� ��� ����� � ��� �� ������ � �� ������������ ���������� �����. 
  
����� ������ �������� ������ �� ���������, ������� ������������� ������ �������������� �������� �������. ��� ��� ����� ������ �������� ������, � �� ����������� ���������, ��� �������� ���������� ������ ��� ������. ��� �� ����� ��������� ������ ����� ��� ��������� ��� ����� ����������� ��� ����������� � ���. ��� �� ����� ����� ����� ���������, ��������� � ���; � ��� ���� ������ ����������, ����������� ��� ������������. ��������� ������� �� ����� ������, ���������� ��������� �� �����, ���������� ���������.
  
Тип папки хранится в свойстве **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md)). ������ ����� ��� �������� ����� �������� FOLDER_GENERIC, FOLDER_ROOT ��� FOLDER_SEARCH, � ����������� �� ����.
  
������ ����� ���� ���� ������ �������������� � ���� ���� ������. Идентификатор записи, **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), используется клиентами и поставщиков услуг для откройте папку. Ключ записи, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) — это двоичное значение, которое используется для сравнения папки с другими папками. 
  
����� ����� ������ �������� ��� ������������� ��������� � ���� ����� � ��������� ���������. ���������� ��������� ��������:
  
- **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))
    
- **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))
    
- **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))
    
Свойство **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)), который описывает тип операции, которые пользователь может выполнять поддержка некоторых папок. �������� ���� �� ���������� �������� **PR_ACCESS** � MAPI_ACCESS_DELETE, ��� ��������, ��� ����� ����� ���� �������. ���� ��������, MAPI_ACCESS_MODIFY, ���������, ��� ����� ������ ���� ����� ��������. 
  
������ ������ �������� ����������� ����� � ������� ��������� [IMAPIFolder](imapifolderimapicontainer.md) . 
  
## <a name="see-also"></a>��. �����



[���������� ���������� MAPI](mapi-application-development.md)
