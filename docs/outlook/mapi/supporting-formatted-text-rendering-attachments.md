---
title: ��������� ��������������� ����� ����������� ��������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68abe85b-5dc0-40d0-8917-30ea002aa816
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 14c1162bd4e225fd3ab2ea5ab11536b3bdf08edd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812409"
---
# <a name="supporting-formatted-text-rendering-attachments"></a>��������� ��������������� �����: ����������� ��������

  
  
**Относится к**: Outlook 
  
Клиентское приложение, которое заботится где сообщение его вложения отображаются задает свойство **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) для этих вложений во время сообщения. ��� ������, ������� �� ����� ��������, � ���������� ������������ �������� ��� �������� ����������.
  
������ �������� ��������� � ����������, ��� �������� �������� �������� **PR_RENDERING_POSITION** ������� ��������, ����� ����������, ��� � �������� ������ ���������, � ������� ������ ������������ ��������. ��� ��������� **PR_RENDERING_POSITION**������ ����� ������������ ���� �� ��������� �������:
  
- [IMAPIProp::GetProps](imapiprop-getprops.md) on the open attachment to retrieve the **PR_RENDERING_POSITION** property. 
    
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) on the open message to retrieve its attachment table. **PR_RENDERING_POSITION** is a required column in all attachment tables. This is the preferred method because it results in better performance. 
    
�������� ������� �� �������� RTF ��������� ����� ��������, ������� �� ���������� ������ ��� ��������������� �������� ��� **PR_RENDERING_POSITION**. ��� ��� �������� ��������� ������������� �������� **PR_RENDERING_POSITION** �������� � ����� �� ������ ��� �������� **PR_BODY** ���������, ��������� ������� �� �������� RTF ��������� �������� ������ �������� �������� ����������� ����������� ��� ������ ����������� ������� **PR_BODY**. ��� �������������� �������� �������� ��������� ��������������, �������� ������������ ��� ��������� ������������������ ����� �������� ������� �� �������� RTF ���������. �������������� ��������������, ��������, � �� ������ ���������� ��������� ������� � �������� ����������� � ����������� ��������. 
  
�������� ������� �� �������� RTF ��������� ������� ���������� �� ��������������� ��������, ����������� �� ��������, ����������� �������, ������������� �� �������� ��������. �������� �� ��, ��� ��� ������� ������ ���������� **PR_RENDERING_POSITION**, ����� ����������� ��������� ����������� ����������� �� ���������� ����������� ��������� ���������. ���� ������ �� **PR_RENDERING_POSITION**, ��������� ��������� ����� ������ �������� -1, ����� �������, ��� ��������� �� � ������ ���������. �������� � ���������� ���������-1 ����� ������������ � ����� ����� ������ ��������� � ����������� �� �������. ���������� �������� ��������� ��� ���� �������� � ������� ����� ���������.
  
Степень точности для свойства **PR_RENDERING_POSITION** зависит от того, является ли хранилища сообщений сохраняет сообщение **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) и свойства **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) или только **PR_RTF_COMPRESSED**. ���� ������ ������� **PR_BODY** � ��������� ��� � ��������� ��������� ������ � ���������������� ������, ��������� ������������ ����� �������. ��� �� ����� ���� ��������� ��������� ���������� ������� ����������� ������ **PR_BODY**, ��� ��� �� ��������� ������ **PR_RTF_COMPRESSED**, ��������, ��� ����� ������� �������� ��������� ������������. ��� ��-�� ��������, ��� ������� � ���������� ��������� ��������� ������� �������� **PR_BODY**, ���. 
  
To calculate an accurate **PR_RENDERING_POSITION** value, an RTF-aware store uses a tag embedded in the formatted text. The utility function **RTFSync** can be called to perform this calculation and update an attachment's rendering position. Depending on the amount of state information available, the message store can pass either RTF_SYNC_BODY_CHANGED, RTF_SYNC_RTF_CHANGED, or both values to [RTFSync](rtfsync.md).
  

