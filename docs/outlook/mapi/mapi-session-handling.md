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
ms.openlocfilehash: 98c4bd0dba630db32fdb2309be3d29ebc13b1131
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422063"
---
# <a name="mapi-session-handling"></a>��������� ������ MAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Прежде чем взаимодействовать с поставщиками услуг и системой обмена сообщениями, необходимо установить сеанс. Сеанс MAPI — это ссылка клиента на другие компоненты MAPI. В результате успешного запуска сеанса MAPI возвращает клиентам указатель на объект сеанса , который реализует интерфейс **IMAPISession.** Дополнительные сведения см. в [подразделе IMAPISession : IUnknown](imapisessioniunknown.md). С помощью методов интерфейса **IMAPISession** можно получить доступ к объектам адресной книги и поставщиков хранимых сообщений, получить доступ к нескольким таблицам, отображать формы, устанавливать свойства поставщика транспорта, а также выполнять администрирование профилей и служб сообщений. 
  
## <a name="in-this-section"></a>В этом разделе:

[Запуск сеанса MAPI](starting-a-mapi-session.md)
  
> Описание запуска сеанса MAPI и ссылки на разделы с более подробными сведениями.
    
[Завершение сеанса MAPI](ending-a-mapi-session.md)
  
> Описывает завершение сеанса MAPI.
    
[Доступ к объектам с помощью сеанса](accessing-objects-by-using-the-session.md)
  
> Описывает, как использовать указатель сеанса для доступа к объектам сеанса.
    
[Искомые удостоверения основного и поставщика](retrieving-primary-and-provider-identity.md)
  
> Описывает свойства, используемые для извлечения удостоверения основного и поставщика.
    
[Таблица состояния и объекты состояния](status-table-and-status-objects.md)
  
> Описывает, как получить доступ к сведениям из таблицы состояния.
    

