---
title: Синхронизация текста и форматирования
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435105"
---
# <a name="synchronizing-text-and-formatting"></a>Синхронизация текста и форматирования

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Основной проблемой при отправке сообщений в формате RTF является синхронизация текста с форматированием. Чтобы обеспечить синхронизацию текста и форматирования при направлении сообщений в место назначения и синхронизацию текста и форматирования, MAPI предоставляет функцию [RTFSync.](rtfsync.md) **RTFSync** обычно вызван клиентами с RTF перед отображением входящих сообщений и пулером MAPI при загрузке сообщений поставщику транспорта. Звоняющие указывают область возможных несоответствий, передавая один или два флага **в RTFSync:**
  
- RTF_SYNC_BODY_CHANGED, чтобы указать изменение текста сообщения.
    
- RTF_SYNC_RTF_CHANGED, чтобы указать изменение форматирования сообщений.
    
Процесс синхронизации, который происходит в **RTFSync,** является сложной проверкой циклической избыточности (CRC) текста сообщения, который игнорирует некоторые символы и преобразует другие. Символы, которые, скорее всего, были добавлены поставщиками транспорта, игнорируются. MAPI определяет несколько свойств для работы с RTF, как описано в следующей таблице. 
  
|**Свойство RTF**|**Описание**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag)](pidtagrtfsyncbodytag-canonical-property.md)  <br/> |Указывает начало реального текста сообщения.  <br/> |
|**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc)](pidtagrtfsyncbodycrc-canonical-property.md)  <br/> |Содержит результат циклической проверки избыточности текста сообщения.  <br/> |
|**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount)](pidtagrtfsyncbodycount-canonical-property.md)  <br/> |Содержит количество символов в **PR_RTF_SYNC_BODY_CRC.**  <br/> |
|**PR_RTF_IN_SYNC** ([PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)  <br/> |Установите true, если текст сообщения и форматирование синхронизированы.  <br/> |
|**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount)](pidtagrtfsyncprefixcount-canonical-property.md)  <br/> |Содержит количество символов, не в которых содержится текст сообщения.  <br/> |
|**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount)](pidtagrtfsynctrailingcount-canonical-property.md)  <br/> |Содержит количество символов, не в которых содержится текст сообщения.  <br/> |
   

