---
title: ����������� ����� � �������� ���������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9462070e-1472-4e12-ba4e-e4ac60022892
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: ae881f56695914627e8c2f6f61f143da91cd78a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416764"
---
# <a name="special-folders-in-message-stores"></a>����������� ����� � �������� ���������

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Special folders such as the Inbox, Outbox, and search-results folder may be created in advance and protected by the message store provider. If the folders do not exist, MAPI will attempt to create them in the message store by calling the [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function. For more information, see [����������� ����� MAPI](mapi-special-folders.md).
  
## <a name="see-also"></a>См. также



[Реализация папок в хранилищах сообщений](implementing-folders-in-message-stores.md)

