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
ms.openlocfilehash: 7e33c49d1ed211abf70e04a8bd3c06ca62e88572
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434923"
---
# <a name="supporting-named-properties-in-message-stores"></a>��������� ����������� ������� � �������� ���������

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Message objects can have properties in them that are not in the set of properties defined by MAPI. Such properties can be unnamed or named. Unnamed properties must reside in a range of property identifiers defined by MAPI. Named custom properties reside in a different range of property identifiers defined by MAPI. They are typically used by custom message types. Your message store provider must support named properties if it is to be used as the default message store. Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers. For more information, see [����������� ����� ������� MAPI](defining-new-mapi-properties.md) and [��������� ����������� �������](supporting-named-properties.md).
  
����������� ��������� ��������� �����������, ������� ������������ ������������� ������� ������� ������ ������������� ��� ���� �������� � ��������� ��������� � ������. ��� ����� ��� ������������. ��-������ ����� ����������� �������� �������������, ���� �� ���������� ������ ��� ������������. ��-������ ���� ��� ������� � ��������� ��������� ������������ �� ������� �������������, ���������� ���������� �������������, ��� ��� �������������� ������� �� ��������� � ��������� ��������� ���������� ��������� �� ����� ����������� ��������. ��� ��������� ���������� ����������� ��� ����������� �������� ��� ����������� ������� � �� ������������� �����.
  
## <a name="see-also"></a>См. также



[Включение сообщений в хранилищах сообщений](implementing-messages-in-message-stores.md)

