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
ms.openlocfilehash: 5f03530f994fd13e7dc4c7eaa4124900c28e613b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405298"
---
# <a name="supporting-formatted-text-rendering-attachments"></a>Поддержка форматированного текста: отображение вложений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиентское приложение, которое заботится о том, где в сообщении вложения отображаются, задает свойство **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) для этих вложений во время композиции сообщения. ��� ������, ������� �� ����� ��������, � ���������� ������������ �������� ��� �������� ����������.
  
������ �������� ��������� � ����������, ��� �������� �������� �������� **PR_RENDERING_POSITION** ������� ��������, ����� ����������, ��� � �������� ������ ���������, � ������� ������ ������������ ��������. ��� ��������� **PR_RENDERING_POSITION**������ ����� ������������ ���� �� ��������� �������:
  
- [IMAPIProp::GetProps](imapiprop-getprops.md) on the open attachment to retrieve the **PR_RENDERING_POSITION** property. 
    
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) on the open message to retrieve its attachment table. **PR_RENDERING_POSITION** is a required column in all attachment tables. This is the preferred method because it results in better performance. 
    
�������� ������� �� �������� RTF ��������� ����� ��������, ������� �� ���������� ������ ��� ��������������� �������� ��� **PR_RENDERING_POSITION**. ��� ��� �������� ��������� ������������� �������� **PR_RENDERING_POSITION** �������� � ����� �� ������ ��� �������� **PR_BODY** ���������, ��������� ������� �� �������� RTF ��������� �������� ������ �������� �������� ����������� ����������� ��� ������ ����������� ������� **PR_BODY**. ��� �������������� �������� �������� ��������� ��������������, �������� ������������ ��� ��������� ������������������ ����� �������� ������� �� �������� RTF ���������. �������������� ��������������, ��������, � �� ������ ���������� ��������� ������� � �������� ����������� � ����������� ��������. 
  
�������� ������� �� �������� RTF ��������� ������� ���������� �� ��������������� ��������, ����������� �� ��������, ����������� �������, ������������� �� �������� ��������. �������� �� ��, ��� ��� ������� ������ ���������� **PR_RENDERING_POSITION**, ����� ����������� ��������� ����������� ����������� �� ���������� ����������� ��������� ���������. ���� ������ �� **PR_RENDERING_POSITION**, ��������� ��������� ����� ������ �������� -1, ����� �������, ��� ��������� �� � ������ ���������. �������� � ���������� ���������-1 ����� ������������ � ����� ����� ������ ��������� � ����������� �� �������. ���������� �������� ��������� ��� ���� �������� � ������� ����� ���������.
  
Степень точности для свойства **PR_RENDERING_POSITION** зависит от того, сохраняет ли хранилище сообщений свойства **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) и **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) или только **PR_RTF_COMPRESSED**. ���� ������ ������� **PR_BODY** � ��������� ��� � ��������� ��������� ������ � ���������������� ������, ��������� ������������ ����� �������. ��� �� ����� ���� ��������� ��������� ���������� ������� ����������� ������ **PR_BODY**, ��� ��� �� ��������� ������ **PR_RTF_COMPRESSED**, ��������, ��� ����� ������� �������� ��������� ������������. ��� ��-�� ��������, ��� ������� � ���������� ��������� ��������� ������� �������� **PR_BODY**, ���. 
  
To calculate an accurate **PR_RENDERING_POSITION** value, an RTF-aware store uses a tag embedded in the formatted text. The utility function **RTFSync** can be called to perform this calculation and update an attachment's rendering position. Depending on the amount of state information available, the message store can pass either RTF_SYNC_BODY_CHANGED, RTF_SYNC_RTF_CHANGED, or both values to [RTFSync](rtfsync.md).
  

