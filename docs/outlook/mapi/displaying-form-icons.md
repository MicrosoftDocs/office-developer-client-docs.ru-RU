---
title: Отображение значков форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7ac8026489b06031e07ab4b2978c9ece04063bb1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579146"
---
# <a name="displaying-form-icons"></a>Отображение значков форм

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
При отображении списка сообщений в папке, полезно для пользователей различать сообщения с помощью пользовательских классов сообщений из стандартных IPM. Обратите внимание, сообщения. Настраиваемые классы сообщения соответствуют формы серверы и серверы формы предоставляют значки будет представлять собой. В списке сообщений для оповещения пользователей для каждого сообщения класс сообщения можно отобразить эти значки, прежде чем пользователь открывает сообщения. Как правило значок в свойстве **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) формы, то, которое должно отображаться в списке сообщений. Формы также имеют свойство **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)), которые могут отображаться, когда форма свернута в окне свойств.
  
 **Чтобы получить значок для класса сообщения без активации сервера форм для этого класса сообщений**
  
1. Вызовите метод [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) для получения указателя на [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) интерфейса. 
    
2. Вызовите метод [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) для получения указателя на [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) интерфейса. 
    
3. Вызовите метод [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) для получения дескриптор значка. 
    
Значок могут отображаться с помощью стандартных Win32 API.
  
> [!IMPORTANT]
> При наличии значок класс сообщения, внесите все усилия для кэширования этот значок. Не кэширование значки серьезно влияет на производительность клиентских приложений. При кэшировании значки, следует избегать отношений между классы сообщений и их подклассов. Например если IPM. Класс сообщения Note.Meeting.Cancel происходит для разрешения IPM. Обратите внимание на то, не предполагается, что все подклассов IPM. Примечание следует использовать значок IPM. Примечание. 
  

