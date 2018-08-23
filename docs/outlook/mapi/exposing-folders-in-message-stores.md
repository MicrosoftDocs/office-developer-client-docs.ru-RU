---
title: �������������� ������� � ������ � �������� ���������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 62f50ed7925305eca7432da17130d2be0365ef03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582597"
---
# <a name="exposing-folders-in-message-stores"></a>�������������� ������� � ������ � �������� ���������

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
������ ��������� �������� ��������� ���������� ����������� �������� ������ ���������� [IMAPIFolder](imapifolderimapicontainer.md) ��� ���������� ����������. ������������� ����� �������� ������ � ��������� ��� ���������; ��� ������������� ������ � ������, ������� ����� ������ ������������ ��� ���������� ��������� ���������. ����� ����, ����� �������� ������ ����� ������������ ��� �������� �� ��������� �������� ����� ��� ���������������� �������� ��������� � ��� ����� �� ������� ������ ������������ ������. ���������� ��������� ��������� ����� ���������� ����������� ��������� IPM � ����� �����, ������������ ��� �������� ��������� IPM � �� ���������� ����������. 
  
���������� ���������� ����� ������� ����� �������� ������, ������ ����� [IMsgStore::OpenEntry](imsgstore-openentry.md) � 0 �� NULL ����������  _cbEntryId_ �  _lpEntryId_, ��������������. ��� �� �����, � ����������� ������� ���������� ���������� �������� � ����� �����, ���������� IPM ���������. 
  
����� �������� ������ �����, ������������� � ��������� ��������� IPM ����� ������, ����������� ��������� ���������:
  
1. ����������� ����� MAPI ��� ������ ������ [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . 
    
2. Используйте полученный в результате указатель базы данных сообщений для вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) для свойства **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
3. �������� ����� [IMsgStore::OpenEntry](imsgstore-openentry.md) � ��������������� ������ ��� ��������� ��������� **IMAPIFolder**. 
    
4. �������� ����� [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) ��� ��������� ������� ���������� �����. 
    
5. �������� ����� [IMAPITable::QueryRows](imapitable-queryrows.md) � ������ ����� � ����� �������� ������. 
    
MAPI ������� ���������� ��� ����� ��� ������� � ������ �������� ����� � ��������� �������� � ��������� ���������. **IMAPIFolder**� ��� ������������� ���������� [IMAPIContainer](imapicontainerimapiprop.md)�������� ������, ������� ������ ������������� ���������� ��������� ��������� ��� ���������� ����� � ��������� ��������� � �������� �� ������� ������� ��� ������ � ����������.
  
## <a name="see-also"></a>��. �����



[���������� ����� � �������� ���������](implementing-folders-in-message-stores.md)

