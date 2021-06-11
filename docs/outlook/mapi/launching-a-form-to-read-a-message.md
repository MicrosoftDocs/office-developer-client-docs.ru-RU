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
ms.openlocfilehash: 439927dc78941f086c025d77c76236497d3f4a15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425934"
---
# <a name="launching-a-form-to-read-a-message"></a>Запуск формы для чтения сообщения

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Реализутелям серверов форм следует ожидать следующей последовательности вызовов метода на сервер формы и объекты формы при загрузке клиентского приложения сообщения:
  
1. Клиентская заявка открывает диспетчер форм с вызовом на функцию [MAPIOpenFormMgr.](mapiopenformmgr.md) 
    
2. Клиентская заявка вызывает [метод IMAPIFormMgr::LoadForm,](imapiformmgr-loadform.md) который возвращает объект [с помощью IMAPIForm.](imapiformiunknown.md) Менеджер формы может быть выпущен сейчас, если он не будет использоваться для дальнейших активаций формы. Обратите внимание, что вызов **в LoadForm может** занять некоторое время, так как диспетчеру форм может потребоваться установить исполняемые файлы сервера форм перед началом выполнения. 
    
3. Дополнительно клиентская заявка может подготовить [IMAPIViewContext](imapiviewcontextiunknown.md) для управления операциями, которые могут привести к загрузке объекта формы предыдущего или следующего сообщения в папке. Клиентская заявка может использовать [метод IMAPIForm::SetViewContext](imapiform-setviewcontext.md) для изменения контекста представления по умолчанию, установленного в **вызове LoadForm.** 
    
4. Клиентская заявка вызывает [метод IPersistMessage::Load](ipersistmessage-load.md) для загрузки данных сообщений в объект формы. 
    
5. Клиентская заявка вызывает [IMAPIForm::D oVerb,](imapiform-doverb.md) чтобы вызвать открытый глагол, передав необязательный указатель [интерфейса IMAPIViewContext.](imapiviewcontextiunknown.md) 
    
## <a name="see-also"></a>См. также



[Взаимодействие с сервером форм](form-server-interactions.md)

