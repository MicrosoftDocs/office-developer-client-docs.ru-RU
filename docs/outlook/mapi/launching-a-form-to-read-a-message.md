---
title: Запуск формы для чтения сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b9166090321aa24e35fe1c82908aec0c403095cd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593741"
---
# <a name="launching-a-form-to-read-a-message"></a>Запуск формы для чтения сообщения

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Специалистов по внедрению сервера форм следует ожидать следующую последовательность вызовов их server формы и объекты формы при загрузке клиентского приложения сообщение:
  
1. Клиентское приложение Откроется диспетчер форм с вызова функции [MAPIOpenFormMgr](mapiopenformmgr.md) . 
    
2. Клиентское приложение вызывает метод [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) , который возвращает объект с [IMAPIForm](imapiformiunknown.md). Диспетчер форм может выпущен теперь, если он не будет использоваться для дальнейшей активаций формы. Обратите внимание, что вызов **LoadForm** может занять некоторое время, так как может потребоваться установка исполняемых файлов сервера формы перед тем как диспетчер форм. 
    
3. При необходимости в клиентском приложении можно подготовить [IMAPIViewContext](imapiviewcontextiunknown.md) операциям элемента управления, которые могут привести объект формы для загрузки предыдущему или следующему сообщение в папке. В клиентском приложении можно использовать метод [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) для изменения контекста представления по умолчанию, которое было задано в вызове **LoadForm** . 
    
4. Клиентское приложение вызывает метод [IPersistMessage::Load](ipersistmessage-load.md) для загрузки данных сообщений в объект формы. 
    
5. Клиентское приложение вызывает [IMAPIForm::DoVerb](imapiform-doverb.md) для вызова open команды, передав дополнительный указатель интерфейса [IMAPIViewContext](imapiviewcontextiunknown.md) . 
    
## <a name="see-also"></a>См. также



[Взаимодействие серверов форм](form-server-interactions.md)

