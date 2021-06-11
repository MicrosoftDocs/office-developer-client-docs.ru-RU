---
title: Ведение библиотеки форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 51c7c3f8ba70dcb3d35dc50806e984fd4b193818
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408805"
---
# <a name="maintaining-a-form-library"></a>Ведение библиотеки форм

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Библиотека форм содержит всю важную информацию о форме: ее свойствах, глаголах и исполняемых файлах сервера. Некоторые клиенты позволяют пользователям поддерживать, устанавливать или удалять серверы форм. Если вы хотите предложить эту функцию пользователям, у вас должен быть доступ к:
  
- Файл конфигурации сервера форм, файл с файлом . Расширение CFG.
    
- Контейнерный объект библиотеки форм, объект, который реализует [интерфейс IMAPIFormContainer: IUnknown.](imapiformcontaineriunknown.md) 
    
Чтобы получить доступ к файлу конфигурации или имени пути к нему, используйте любые удобные средства. Обычно клиенты представляют пользователю диалоговое окно для установки и удаления серверов форм, которые также могут быть использованы для запроса пользователя на расположение файла конфигурации.
  
Чтобы получить доступ к контейнеру библиотеки форм, позвоните по методу [IMAPIFormMgr::OpenFormContainer.](imapiformmgr-openformcontainer.md) Передай в значении переоформления, чтобы указать, какую библиотеку форм открыть, а при необходимости - указатель на объект, который должен использовать руководитель форм для открытия библиотеки форм. Например, если вы открываете библиотеки форм [папок,](folder-form-libraries.md)передай [указатель IMAPIFolder: IMAPIContainer.](imapifolderimapicontainer.md) 
  
После того как **OpenFormContainer** возвращает указатель **IMAPIFormContainer,** позвоните либо [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) или [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), в зависимости от выполняемого обслуживания. **InstallForm** добавляет сервер формы в библиотеку; **RemoveForm** удаляет сервер формы из библиотеки. 
  

