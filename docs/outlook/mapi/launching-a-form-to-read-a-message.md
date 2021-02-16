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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
При загрузке сообщения клиентского приложения для реализации сервера форм следует ожидать следующей последовательности вызовов методов к их серверам форм и объектам форм:
  
1. Клиентские приложения открывают диспетчер форм с помощью вызова [функции MAPIOpenFormMgr.](mapiopenformmgr.md) 
    
2. Клиентские приложения вызывает [метод IMAPIFormMgr::LoadForm,](imapiformmgr-loadform.md) который возвращает объект [с IMAPIForm](imapiformiunknown.md). Диспетчер форм может быть освобожден, если он не будет использоваться для дальнейшей активации формы. Обратите внимание, что вызов **LoadForm** может занять некоторое время, так как диспетчеру форм может потребоваться установить исполняемые файлы сервера форм перед выполнением. 
    
3. При желании клиентские приложения могут подготовить [IMAPIViewContext](imapiviewcontextiunknown.md) для управления операциями, которые могут привести к загрузке объекта формы предыдущего или следующего сообщения в папку. Клиентские приложения могут использовать [метод IMAPIForm::SetViewContext](imapiform-setviewcontext.md) для изменения контекста представления по умолчанию, который был установлен в **вызове LoadForm.** 
    
4. Клиентские приложения вызывает [метод IPersistMessage::Load](ipersistmessage-load.md) для загрузки данных сообщения в объект формы. 
    
5. Клиентские приложения вызывают [IMAPIForm::D oVerb](imapiform-doverb.md) для вызова открытой команды, передавая необязательный указатель интерфейса [IMAPIViewContext.](imapiviewcontextiunknown.md) 
    
## <a name="see-also"></a>См. также



[Взаимодействие с сервером форм](form-server-interactions.md)

