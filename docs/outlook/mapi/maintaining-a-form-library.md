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
ms.openlocfilehash: 51c7c3f8ba70dcb3d35dc50806e984fd4b193818
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408805"
---
# <a name="maintaining-a-form-library"></a>Обслуживание библиотеки форм

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Библиотека форм содержит все важные сведения о форме: ее свойства, команды и исполняемые файлы сервера. Некоторые клиенты позволяют своим пользователям обслуживать, устанавливать или удалять серверы форм. Если вы хотите предложить эту функцию пользователям, у вас должен быть доступ к:
  
- Файл конфигурации сервера форм, файл с файлом . Расширение CFG.
    
- Объект контейнера библиотеки форм, который реализует [интерфейс IMAPIFormContainer : IUnknown.](imapiformcontaineriunknown.md) 
    
Чтобы получить к нему доступ к файлу конфигурации или имени пути, используйте любые удобные средства. Обычно клиенты представляют пользователю диалоговое окно для установки и удаления серверов форм, которое также можно использовать для запроса расположения файла конфигурации.
  
Чтобы получить доступ к контейнеру библиотеки форм, вызовите метод [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) диспетчера форм. Передав значение из enumeration, укажите, какую библиотеку форм следует открыть, и при необходимости указатель на объект, который диспетчер форм должен использовать для открытия библиотеки форм. Например, если вы открываете библиотеки форм [папок,](folder-form-libraries.md)передав [указатель IMAPIFolder : IMAPIContainer.](imapifolderimapicontainer.md) 
  
После того как **OpenFormContainer** вернет указатель **IMAPIFormContainer,** вызовите [либо IMAPIFormContainer::InstallForm,](imapiformcontainer-installform.md) либо [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), в зависимости от выполняемого обслуживания. **InstallForm** добавляет сервер форм в библиотеку; **RemoveForm** удаляет сервер форм из библиотеки. 
  

