---
title: ��������� ����������� ������� � �������� ���������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1c73bb5-b44a-4ec6-89e4-0e2228572b2d
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: b1aa0228cdc8cf6f0b2bb321e62e40127775a6de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812420"
---
# <a name="supporting-named-properties-in-message-stores"></a>��������� ����������� ������� � �������� ���������

  
  
**Относится к**: Outlook 
  
Message objects can have properties in them that are not in the set of properties defined by MAPI. Such properties can be unnamed or named. Unnamed properties must reside in a range of property identifiers defined by MAPI. Named custom properties reside in a different range of property identifiers defined by MAPI. They are typically used by custom message types. Your message store provider must support named properties if it is to be used as the default message store. Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers. For more information, see [����������� ����� ������� MAPI](defining-new-mapi-properties.md) and [��������� ����������� �������](supporting-named-properties.md).
  
����������� ��������� ��������� �����������, ������� ������������ ������������� ������� ������� ������ ������������� ��� ���� �������� � ��������� ��������� � ������. ��� ����� ��� ������������. ��-������ ����� ����������� �������� �������������, ���� �� ���������� ������ ��� ������������. ��-������ ���� ��� ������� � ��������� ��������� ������������ �� ������� �������������, ���������� ���������� �������������, ��� ��� �������������� ������� �� ��������� � ��������� ��������� ���������� ��������� �� ����� ����������� ��������. ��� ��������� ���������� ����������� ��� ����������� �������� ��� ����������� ������� � �� ������������� �����.
  
## <a name="see-also"></a>��. �����



[���������� ��������� � �������� ���������](implementing-messages-in-message-stores.md)

