---
title: Роль поставщика транспорта в подсистеме MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7659369a-0952-4f5a-a86b-91958c4c1a3f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7ea60b73fb1abe32b6db5e3c73d6ef3fac53d35d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812508"
---
# <a name="transport-provider-role-in-the-mapi-subsystem"></a>Роль поставщика транспорта в подсистеме MAPI
  
**Относится к**: Outlook 
  
Библиотеки динамической компоновки (DLL) для транспорта поставщик предоставляет интерфейс между диспетчер очереди MAPI и частью системы обмена сообщениями отвечает за отправки и получения сообщений. Диспетчер очереди MAPI и поставщика транспорта работают вместе для обработки обязанности сообщение или отправку сообщения. Диспетчер очереди MAPI загружает библиотеку DLL поставщика транспорта при первом использовании и освобождает его, если они больше не нужны. Несколько поставщиков транспорта можно установить на том же компьютере, но MAPI предоставляет необходимые одной очереди.
  
Клиентские приложения не обычно связь непосредственно с поставщика транспорта. Вместо этого клиентов отправки сообщений с помощью поставщика хранилища и диспетчер очереди MAPI отправляет исходящих сообщений на соответствующие транспорт и доставляет входящих сообщений в хранилище соответствующего сообщения. Диспетчер очереди MAPI работы и делает его вызовы поставщиками транспорта, если приложения переднего плана, простоя. После при необходимости отображение диалоговых окон при первом поставщика транспорта входа в систему, поставщиками транспорта работать в фоновом режиме до вызова клиентом flush отправлять и получать очереди. 
  
Поставщики транспорта иметь следующие обязанности в MAPI, системы обмена сообщениями:
  
- Регистрация типов адресов, которое они могут принять диспетчер очереди MAPI, диспетчер очереди MAPI можно отправлять сообщения, чтобы поставщик соответствующие транспорта в зависимости от адреса сообщений. Один поставщик транспорта можно регистрировать несколько типов адресов. Поставщики транспорта также можно зарегистрировать адреса определенным получателям с очередью MAPI. Сообщения, адресованные одного из указанных адресов будет отправлен поставщика транспорта, зарегистрированное адрес очереди MAPI. Для получения дополнительных сведений см [поставщика транспорта и модель действующие очереди MAPI](transport-provider-and-mapi-spooler-operational-model.md).
    
- Доставлять входящих сообщений очереди MAPI. В зависимости от особенностей системы обмена сообщениями поставщика транспорта можно либо напрямую сообщить диспетчер очереди MAPI при поступлении сообщения или его можно запросить, что диспетчер очереди MAPI опроса службы транспорта периодически для проверки наличия новых сообщений.
    
- Преобразование свойства сообщений MAPI и из свойства сообщения в определенном системы обмена сообщениями. Например поставщика транспорта может потребоваться преобразование адреса отправителя и получателя в исходящих сообщений в форме, которая является приемлемым системы обмена сообщениями. Некоторые системы обмена сообщениями не поддерживают все свойства сообщения MAPI. Дополнительные сведения о сохранении свойства сообщений MAPI при доставке сообщения системы обмена сообщениями можно [Разработка поставщика транспорта TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md).
    
- Регистрация сообщений и получателей параметры, характерные для поставщика транспорта.
    
- Выполните все проверки учетные данные, необходимые для системы обмена сообщениями.
    
- Access исходящих сообщений с помощью объекта сообщение передается ему по очереди MAPI.
    
- Переведите формат сообщений, если это нужно системы обмена сообщениями.
    
- Уведомите диспетчер очереди MAPI список получателей, которые исходящего поставщика транспорта принял ответственность за обработку путем установки свойства **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) для этих получателей сообщения.
    
- Проинформируйте диспетчер очереди MAPI, когда входящее сообщение необходимо обрабатывать.
    
- Передайте данные входящих сообщений очереди MAPI с помощью объектов сообщений.
    
- Назначьте значения все необходимые свойства сообщения MAPI для входящих сообщений.
    
- Удалите сообщение системы обмена сообщениями после доставки, если это необходимо.
    
- Предоставляют сведения о состоянии для очереди и клиентских приложений MAPI.
    
На следующем рисунке показана роль поставщика транспорта для других компонентов архитектуры MAPI.
  
**Роль поставщика транспорта в системе обмена сообщениями**
  
![Роль поставщика транспорта в системе обмена сообщениями] (media/xp01.gif "Роль поставщика транспорта в системе обмена сообщениями")
  
