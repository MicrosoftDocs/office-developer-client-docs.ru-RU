---
title: �������� � ��������� ����� � �������� ���������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8e4ce129-137d-4618-80a6-88781a578d01
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 6781209cd1bf87f4becf1893b7cba5618549fbce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582891"
---
# <a name="inbox-and-outbox-folders-in-message-stores"></a>�������� � ��������� ����� � �������� ���������

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
��� �������� ��������� �� ���������, ���������� ����������� ����� "��������" � ��������� ����� ���������� ��������� ���������. ��� �������, ��� �������� � ��������� IPM ��������� ���������. ��� ����� ���������� ���, ��� ��� ������������ ��� �����, ��� ��������� ������������ � ���������, �� �� ����������� ������� ��������� �� ���. �������� � ��������� ��������� ���������� ����� �������� ������������������ ������������ ������� ����� ����������� ������������, ��������� ������� MAPI � ���������� ��������� ���������. �������� � ��������� ����� � ��� ������ �����, ������� ������������ ��� �������� ��������� � ������� ���� ������� ������������������. �����, ��, ��� ����� � ��� ����������� ��� ���� � ���, ��� ��� ���������� �������� � ���������; �����, ��� ��������� �������� ��������� ��� ������������ ��� ����� ��������� ��� �������� � ��������� ���������.
  
To support receiving messages, the message store provider must implement the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods. For more information, see [��������� ��������� � ������� ����������� ��������� ���������](receiving-messages-by-using-message-store-providers.md).
  
To support sending messages, the message store provider must support the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method, in addition to the other methods used by the MAPI spooler during the message sending process. A message store's outgoing queue does not have to correspond to an actual folder anywhere in the message store's folder tree. However, it is customary for a message store provider to show the contents of the outgoing message queue in the Outbox folder, if there is one. Doing so gives client applications a convenient way to indicate the status of messages that the user has sent, because an Outbox folder can be displayed along with all the other folders in a message store. For more information, see [�������� ��������� � ������� ����������� ��������� ���������](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>��. �����



[���������� ����� � �������� ���������](implementing-folders-in-message-stores.md)

