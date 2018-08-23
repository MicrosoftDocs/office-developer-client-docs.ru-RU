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
ms.openlocfilehash: d797932a9fd22944f1cfd78e7fb67cd3ddbf8632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588820"
---
# <a name="synchronizing-text-and-formatting"></a>Синхронизация текста и форматирования

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Основная проблема при отправке сообщения форматированный текст (RTF) — это поддержание синхронизации с форматирования текста. Для обеспечения при получении сообщения в место назначения они их авторства предназначен и форматирование текста и синхронизируются, MAPI предоставляет функцию [RTFSync](rtfsync.md) . **RTFSync** обычно вызывается с поддержкой RTF клиентов перед отображением входящих сообщений и диспетчером очереди MAPI, когда загружает сообщения поставщика транспорта. Вызывающие задать область возможных несоответствие, передав одним или двумя флаги **RTFSync**:
  
- RTF_SYNC_BODY_CHANGED для указания изменения в текст сообщения.
    
- RTF_SYNC_RTF_CHANGED для указания изменения в обычный текст.
    
Процесс синхронизации, что происходит в **RTFSync** — проверка сложных циклической (контрольной СУММЫ) текста сообщения, игнорирует некоторые символы и преобразовывает другим пользователям. Символы, вероятнее всего, добавленные поставщиками транспорта игнорируются. MAPI определяет несколько свойств для работы с RTF, как описано в следующей таблице. 
  
|**Свойство RTF**|**Описание**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |Указывает начало текста настоящего сообщения.  <br/> |
|**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |Содержит результат проверки циклической текста сообщения.  <br/> |
|**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |Содержит число знаков в **PR_RTF_SYNC_BODY_CRC**.  <br/> |
|**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))  <br/> |Задайте значение TRUE, когда сообщение синхронизированные текста и форматирования.  <br/> |
|**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |Содержит число знаков nonwhitespace, следует ставить перед ним текста сообщения.  <br/> |
|**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |Содержит число знаков nonwhitespace, аудита текста сообщения.  <br/> |
   

