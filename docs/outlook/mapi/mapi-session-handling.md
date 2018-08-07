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
ms.openlocfilehash: cdf3052175870287ff1a66d3745e90f8b8fff256
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809833"
---
# <a name="mapi-session-handling"></a>��������� ������ MAPI

  
  
**Относится к**: Outlook 
  
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
    

