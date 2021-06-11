---
title: Отправка и получение уведомлений о форме
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4ee47b51a98cf732f4e9af2a87fa1734a7250208
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431857"
---
# <a name="sending-and-receiving-form-notifications"></a>Отправка и получение уведомлений о форме

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Уведомления форм используются в MAPI для облегчения связи как от формы к вашему зрителю, так и от зрителя к форме.
  
Формы отправляют уведомления вашему зрителю при одном из следующих событий:
  
- Форма закрыта.
    
- Новое сообщение загружается в форму.
    
- Операция сохранения завершена.
    
- Отправляется сообщение.
    
Каждый из этих типов событий соответствует определенному методу [в IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), одному из интерфейсов, которые должен реализовать ваш зритель форм. Когда происходит событие, форма вызывает соответствующий **метод IMAPIViewAdviseSink** в раковине рекомендации вашего зрителя. Например, когда появится новое сообщение, которое должен включить в дисплей ваш зритель, форма вызывает метод [IMAPIViewAdviseSink::OnNewMessage.](imapiviewadvisesink-onnewmessage.md) 
  
Реализация представления советую раковину таким образом, что имеет смысл для вашего зрителя; стандартная реализация не существует. Например, в **OnNewMessage** можно обновить представление таблицы содержимого текущей папки, чтобы включить новое сообщение. В [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md)метод, который называется при приеме отправленного события сообщения, можно скопировать отправленное сообщение в папку Отправленные элементы.
  
Формы получают уведомление от зрителя, когда происходит изменение, которое влияет на форму и при загрузке нового сообщения. Чтобы уведомить форму, позвоните по одному из методов **IMAPIFormAdviseSink:** [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) или [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md). Call **OnChange** для обмена данными. Например, если форма отображает последний элемент в папке при прибытии нового сообщения, позвоните **в OnChange** со VCSTATUS_NEXT флагом, чтобы сообщить форме, что теперь есть следующий элемент. 
  
**Вызывай OnActivateNext,** чтобы предупредить форму о поступлении нового сообщения, которое может отображаться или не отображаться. Передай класс сообщений в **OnActivateNext.** 
  
Уведомления объекта формы клиентского приложения обрабатываются интерфейсом **IMAPIViewAdviseSink** клиентского приложения. Дополнительные сведения см. [в iMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).
  

