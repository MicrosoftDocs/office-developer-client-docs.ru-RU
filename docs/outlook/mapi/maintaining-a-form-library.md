---
title: Обслуживание библиотеки форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6713055837e3b9b664d5fa1465c9a889919ee5ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590094"
---
# <a name="maintaining-a-form-library"></a>Обслуживание библиотеки форм

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Библиотека форм хранит все важные сведения об формы: его свойства, его команды и его сервер исполняемых файлов. Некоторые клиенты их пользователи могли поддерживать, Установка и удаление серверов формы. Если вы хотите предлагать этой функции для пользователей, должны иметь доступ к:
  
- Файл конфигурации сервера форм, файла с помощью. Расширение CFG.
    
- Объект-контейнер библиотеки форм, объект, реализующий [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) интерфейса. 
    
Для доступа к файлу конфигурации или путь к нему, использование удобны доступным способом. Как правило клиенты предоставить пользователю диалогового окна Установка и удаление серверов форм, которые также могут использоваться для запроса пользователя для расположения файла конфигурации.
  
Для доступа к container библиотека форм, вызовите метод [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) диспетчер форм. Передайте значение перечисления, чтобы указать, какие библиотеки форм, чтобы открыть и при необходимости указатель на объект, который необходимо использовать диспетчер форм, чтобы открыть библиотеку форм. Например, при открытии [Библиотеки форм папки](folder-form-libraries.md)передать [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) указателя. 
  
После **OpenFormContainer** возвращает указатель **IMAPIFormContainer** , вызовите [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) или [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), в зависимости от обслуживания необходимо выполнить. **InstallForm** Добавление сервера формы в библиотеке. **RemoveForm** удаление сервера формы из библиотеки. 
  

