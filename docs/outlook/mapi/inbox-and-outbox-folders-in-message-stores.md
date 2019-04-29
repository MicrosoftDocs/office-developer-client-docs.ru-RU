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
ms.openlocfilehash: 95a2b7b9bac11404817fb6848d58c45251c141f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414244"
---
# <a name="inbox-and-outbox-folders-in-message-stores"></a>�������� � ��������� ����� � �������� ���������

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
��� �������� ��������� �� ���������, ���������� ����������� ����� "��������" � ��������� ����� ���������� ��������� ���������. ��� �������, ��� �������� � ��������� IPM ��������� ���������. ��� ����� ���������� ���, ��� ��� ������������ ��� �����, ��� ��������� ������������ � ���������, �� �� ����������� ������� ��������� �� ���. �������� � ��������� ��������� ���������� ����� �������� ������������������ ������������ ������� ����� ����������� ������������, ��������� ������� MAPI � ���������� ��������� ���������. �������� � ��������� ����� � ��� ������ �����, ������� ������������ ��� �������� ��������� � ������� ���� ������� ������������������. �����, ��, ��� ����� � ��� ����������� ��� ���� � ���, ��� ��� ���������� �������� � ���������; �����, ��� ��������� �������� ��������� ��� ������������ ��� ����� ��������� ��� �������� � ��������� ���������.
  
To support receiving messages, the message store provider must implement the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods. For more information, see [��������� ��������� � ������� ����������� ��������� ���������](receiving-messages-by-using-message-store-providers.md).
  
To support sending messages, the message store provider must support the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method, in addition to the other methods used by the MAPI spooler during the message sending process. A message store's outgoing queue does not have to correspond to an actual folder anywhere in the message store's folder tree. However, it is customary for a message store provider to show the contents of the outgoing message queue in the Outbox folder, if there is one. Doing so gives client applications a convenient way to indicate the status of messages that the user has sent, because an Outbox folder can be displayed along with all the other folders in a message store. For more information, see [�������� ��������� � ������� ����������� ��������� ���������](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>См. также



[Реализация папок в хранилищах сообщений](implementing-folders-in-message-stores.md)

