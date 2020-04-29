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
  
Прежде чем вы сможете общаться с поставщиками услуг и базовой системой обмена сообщениями, необходимо установить сеанс. Сеанс MAPI представляет собой ссылку от клиента к другим компонентам MAPI. В результате успешного запуска сеанса MAPI возвращает на клиентские указатели на объект Session — объект, который реализует интерфейс **IMAPISession** . Дополнительные сведения см. в статье [IMAPISession: IUnknown](imapisessioniunknown.md). Вы можете использовать методы интерфейса **IMAPISession** для доступа к объектам адресной книги и поставщиков хранилищ сообщений, доступа к нескольким таблицам, формам отображения, настройкам свойств поставщика транспорта, а также для выполнения администрирования службы профилей и сообщений. 
  
## <a name="in-this-section"></a>В этом разделе

[Запуск сеанса MAPI](starting-a-mapi-session.md)
  
> Описывается запуск сеанса MAPI и ссылки на разделы с более подробными сведениями.
    
[Завершение сеанса MAPI](ending-a-mapi-session.md)
  
> Описание завершения сеанса MAPI.
    
[Доступ к объектам с помощью сеанса](accessing-objects-by-using-the-session.md)
  
> Сведения об использовании указателя сеансов для доступа к объектам Session.
    
[Получение основного удостоверения и удостоверения поставщика](retrieving-primary-and-provider-identity.md)
  
> Описывает свойства, используемые для извлечения основного удостоверения и удостоверения поставщика.
    
[Объекты "таблица состояния" и "состояние"](status-table-and-status-objects.md)
  
> Сведения о том, как получить доступ к сведениям из таблицы "состояние".
    

