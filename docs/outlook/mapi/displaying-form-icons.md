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
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438633"
---
# <a name="displaying-form-icons"></a>Отображение значков форм

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
При отображе списка сообщений в папке пользователям будет полезно отличить сообщения от настраиваемого класса сообщений от стандартного IPM. Сообщения заметок. Настраиваемые классы сообщений соответствуют серверам форм, а серверы форм предоставляют значки для представления себя. Вы можете отобразить эти значки в списке сообщений, чтобы предупредить пользователей о каждом классе сообщений, прежде чем пользователь откроет сообщения. Обычно значок в свойстве PR_MINI_ICON **(** [PidTagMiniIcon)](pidtagminiicon-canonical-property.md)— это значок, который должен отображаться в списке сообщений. Формы также имеют **свойство PR_ICON** ([PidTagIcon),](pidtagicon-canonical-property.md)которое может отображаться, когда форма свернута на листе свойств.
  
 **Чтобы получить значок для класса сообщений без активации сервера форм для этого класса сообщений**
  
1. Вызовите метод [IMAPIFormMgr::OpenFormContainer,](imapiformmgr-openformcontainer.md) чтобы получить указатель на [интерфейс IMAPIFormContainer : IUnknown.](imapiformcontaineriunknown.md) 
    
2. Вызовите метод [IMAPIFormContainer::ResolveMessageClass,](imapiformcontainer-resolvemessageclass.md) чтобы получить указатель на [интерфейс IMAPIFormInfo : IMAPIProp.](imapiforminfoimapiprop.md) 
    
3. Вызовите [метод IMAPIFormInfo::MakeIconFromBinary,](imapiforminfo-makeiconfrombinary.md) чтобы получить handle значка. 
    
Значок можно отобразить с помощью стандартных API Win32.
  
> [!IMPORTANT]
> После того как у вас есть значок для класса сообщений, приделайте все возможное, чтобы кэшработать этот значок. Не кэшировка значков серьезно влияет на производительность клиентских приложений. При кэшинге значков будьте осторожны с отношениями между классами сообщений и их подклассами. Например, если IPM. Класс сообщения Note.Meeting.Cancel возвращается к IPM. Обратите внимание, что не предполагается, что все подклассы IPM. Обратите внимание, что значок следует использовать для IPM. Примечание. 
  

