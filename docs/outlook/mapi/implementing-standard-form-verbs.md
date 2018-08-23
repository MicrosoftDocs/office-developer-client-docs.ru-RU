---
title: Реализация стандартных команд для форм
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 46585859e1dde4ecf38262f99cac5e3a9d29e5db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568751"
---
# <a name="implementing-standard-form-verbs"></a>Реализация стандартных команд для форм

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
MAPI определяет набор стандартных команд или действия в случае, если пользователь выбирает элемент меню или нажатии кнопки, поддерживающая всем пользователям формы. Каждый имеет константа, связанные с ним для идентификации, определенных в EXCHFORM. Файл заголовка. В следующей таблице приведены команды стандартной формы и их связанных констант:
  
|**Глагол**|**Значение**|
|:-----|:-----|
|Open  <br/> |EXCHIVERB_OPEN  <br/> |
|Ответить  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|Ответить всем  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Переслать  <br/> |EXCHIVERB_FORWARD  <br/> |
|Print  <br/> |EXCHIVERB_PRINT  <br/> |
|Сохранить как  <br/> |EXCHIVERB_SAVEAS  <br/> |
|Ответ в папку  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
Если пользователь выбирает команду, передайте его константу вызов метода [IMAPIForm::DoVerb](imapiform-doverb.md) формы для его соответствующих действий. 
  
В дополнение к доступ к команд с помощью средства просмотра вашей формы, в некоторых случаях пользователям глаголов непосредственно из формы. К примеру некоторые объекты формы пользователь может вызвать глаголов **Print** , щелкнув правой кнопкой мыши на форме и выберите команду **Печать** контекстное меню. 
  

