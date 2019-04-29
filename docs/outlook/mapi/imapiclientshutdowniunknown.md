---
title: Метод imapiclientshutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown
api_type:
- COM
ms.assetid: b6a5096f-ad27-48b3-b569-f33efc20fa72
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435336"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Позволяет клиенту MAPI выполнять быстрое завершение работы клиентского процесса. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Предоставлено:  <br/> |Объект [IMAPISession](imapisessioniunknown.md)  <br/> |
|Реализовано в:  <br/> |Подсистема MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиент MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_имапиклиентшутдовн  <br/> |
|Тип указателя:  <br/> |ЛПМАПИКЛИЕНТШУТДОВН  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |ЗаПрашивает подсистему MAPI для поддержки быстрого завершения работы, предоставляемой загруженными поставщиками MAPI.  <br/> |
|[Нотифипроцессшутдовн](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Указывает на намерение клиента MAPI выполнить завершение работы.  <br/> |
|[Дофастшутдовн](imapiclientshutdown-dofastshutdown.md) <br/> |Указывает на намерение клиента MAPI немедленно выйти из клиентского процесса.  <br/> |
   
## <a name="remarks"></a>Примечания

Цель быстрого завершения работы состоит в том, чтобы разрешить клиенту MAPI и любому загруженному поставщику MAPI, с которым клиент MAPI имеет активный сеанс MAPI для сохранения параметров и данных MAPI. Это позволяет клиенту MAPI отключить все внешние ссылки и выйти, не вызывая потери данных. Клиент MAPI, который должен выполнять быстрое завершение работы, должен использовать интерфейс **метод imapiclientshutdown** . Клиент MAPI может получить указатель на этот интерфейс, вызвав метод IUnknown:: QueryInterface для любого объекта [IMAPISession](imapisessioniunknown.md) . 
  
Клиент MAPI всегда инициирует быстрое завершение работы путем вызова метода **метод imapiclientshutdown:: QueryFastShutdown** . Подсистема MAPI реагирует на запрос клиента MAPI, проверяя, поддерживает ли загруженные поставщики MAPI быстрое завершение работы клиента. Администратор может использовать параметры реестра Windows, чтобы определить уровень поддержки поставщика, который необходим для работы клиентов MAPI с быстрым завершением работы. Дополнительные сведения приведены в разделе [Параметры быстрого завершения работы пользователя](fast-shutdown-user-options.md).
  
Для продолжения быстрого завершения работы клиент вызывает метод **метод imapiclientshutdown:: нотифипроцессшутдовн** , который указывает на подсистему MAPI намерение завершить работу. Затем клиент вызывает метод **метод imapiclientshutdown::D офастшутдовн** , чтобы указать, что клиентский процесс завершается немедленно. 
  
Дополнительные сведения о быстром завершении работы приведены в разделе [Обзор быстрого завершения работы](fast-shutdown-overview.md). Для получения сведений о выполнении быстрого завершения работы ознакомьтесь со статьями [рекомендации по быстроМу завершенИю работы](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)
  
[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

