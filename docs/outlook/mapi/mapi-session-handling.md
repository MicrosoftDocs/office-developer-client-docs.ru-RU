---
title: ��������� ������ MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8c82ff28dca4fc50c7801a533f7ad757b839cddf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568233"
---
# <a name="mapi-session-handling"></a>��������� ������ MAPI

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Прежде чем можно общаться с поставщиками услуг и системы обмена сообщениями, необходимо установить сеанс. Сеанс MAPI — это ссылка из клиента на другие компоненты MAPI. В результате успешного запуска сеанса MAPI возвращает клиентам указатель на объект сеанса — это объект, реализующий интерфейс **IMAPISession** . Дополнительные сведения можно [IMAPISession: IUnknown](imapisessioniunknown.md). Можно использовать методы интерфейса **IMAPISession** доступа к объектам поставщиков хранилища адресной книги и сообщения, доступ к несколько таблиц, отображение форм, свойства поставщика транспорта и выполнять администрирование службы профилей и сообщения. 
  
## <a name="in-this-section"></a>В этой статье

[Запуск сеанса MAPI](starting-a-mapi-session.md)
  
> Описывается, как начать сеанс MAPI и содержит ссылки на разделы с более подробными сведениями.
    
[Завершение сеанса MAPI](ending-a-mapi-session.md)
  
> Описывается, как завершить сеанс MAPI.
    
[Доступ к объектам с помощью сеанса](accessing-objects-by-using-the-session.md)
  
> Описывается, как использовать указатель сеанса для доступа к объектам сеанса.
    
[Получение удостоверения поставщика и основного удостоверения](retrieving-primary-and-provider-identity.md)
  
> Описываются свойства, используемые для получения основной и поставщика удостоверений.
    
[Таблица и объекты состояний](status-table-and-status-objects.md)
  
> Описывается, как получить доступ к информации из таблицы состояния.
    

