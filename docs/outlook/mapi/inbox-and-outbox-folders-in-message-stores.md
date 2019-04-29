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
# <a name="inbox-and-outbox-folders-in-message-stores"></a><span data-ttu-id="6c37b-103">�������� � ��������� ����� � �������� ���������</span><span class="sxs-lookup"><span data-stu-id="6c37b-103">Inbox and Outbox Folders in Message Stores</span></span>

  
  
<span data-ttu-id="6c37b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c37b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c37b-p101">��� �������� ��������� �� ���������, ���������� ����������� ����� "��������" � ��������� ����� ���������� ��������� ���������. ��� �������, ��� �������� � ��������� IPM ��������� ���������. ��� ����� ���������� ���, ��� ��� ������������ ��� �����, ��� ��������� ������������ � ���������, �� �� ����������� ������� ��������� �� ���. �������� � ��������� ��������� ���������� ����� �������� ������������������ ������������ ������� ����� ����������� ������������, ��������� ������� MAPI � ���������� ��������� ���������. �������� � ��������� ����� � ��� ������ �����, ������� ������������ ��� �������� ��������� � ������� ���� ������� ������������������. �����, ��, ��� ����� � ��� ����������� ��� ���� � ���, ��� ��� ���������� �������� � ���������; �����, ��� ��������� �������� ��������� ��� ������������ ��� ����� ��������� ��� �������� � ��������� ���������.</span><span class="sxs-lookup"><span data-stu-id="6c37b-p101">To be the default message store, a message store provider must implement Inbox and Outbox folders. They are typically stored in the IPM subtree of a message store. These folders are special in that they are designated as the folders that messages are delivered to and sent from, but no special functionality is required of them. Sending and receiving messages happens by way of defined call sequences between client applications, the MAPI spooler, and the message store provider. The Inbox and Outbox folders are simply folders that are used to hold messages during those call sequences. The important point is not that the folders are special, or even that they are named Inbox and Outbox; the important point is that the message store provider uses them as part of its support for sending and receiving messages.</span></span>
  
<span data-ttu-id="6c37b-p102">To support receiving messages, the message store provider must implement the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods. For more information, see [��������� ��������� � ������� ����������� ��������� ���������](receiving-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="6c37b-p102">To support receiving messages, the message store provider must implement the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods. For more information, see [Receiving Messages by Using Message Store Providers](receiving-messages-by-using-message-store-providers.md).</span></span>
  
<span data-ttu-id="6c37b-p103">To support sending messages, the message store provider must support the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method, in addition to the other methods used by the MAPI spooler during the message sending process. A message store's outgoing queue does not have to correspond to an actual folder anywhere in the message store's folder tree. However, it is customary for a message store provider to show the contents of the outgoing message queue in the Outbox folder, if there is one. Doing so gives client applications a convenient way to indicate the status of messages that the user has sent, because an Outbox folder can be displayed along with all the other folders in a message store. For more information, see [�������� ��������� � ������� ����������� ��������� ���������](sending-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="6c37b-p103">To support sending messages, the message store provider must support the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method, in addition to the other methods used by the MAPI spooler during the message sending process. A message store's outgoing queue does not have to correspond to an actual folder anywhere in the message store's folder tree. However, it is customary for a message store provider to show the contents of the outgoing message queue in the Outbox folder, if there is one. Doing so gives client applications a convenient way to indicate the status of messages that the user has sent, because an Outbox folder can be displayed along with all the other folders in a message store. For more information, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6c37b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="6c37b-118">See also</span></span>



[<span data-ttu-id="6c37b-119">Реализация папок в хранилищах сообщений</span><span class="sxs-lookup"><span data-stu-id="6c37b-119">Implementing Folders in Message Stores</span></span>](implementing-folders-in-message-stores.md)

