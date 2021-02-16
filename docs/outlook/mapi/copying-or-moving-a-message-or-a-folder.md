---
title: Копирование или перемещение сообщения или папки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413502"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>Копирование или перемещение сообщения или папки
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиент может использовать один из четырех методов копирования или перемещения сообщения или папки:
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
Установив соответствующие флаги и параметры, **CopyTo** и **CopyProps** можно сделать так же, как **CopyFolder** или **CopyMessages.** При выборе метода вызова учитывайте следующие проблемы:
  
- Копируете или перемещаете папку или сообщение?
    
- Сколько вы знаете о папке или сообщении, которые необходимо скопировать?
    
- Сколько свойств папки или сообщения будет перемещено или скопировано?
    
Методы **IMAPIProp** можно использовать для копирования или перемещения папки или сообщения. **IMAPIFolder::CopyMessages** работает только с сообщениями; **IMAPIFolder::CopyFolder работает** только с папками. 
  
В то время как для использования методов **IMAPIFolder** не требуется знание свойств, поддерживаемых папкой или сообщением для копирования или перемещений, для использования методов **IMAPIProp** необходимы некоторые знания. С **помощью IMAPIProp::CopyProps** необходимо иметь возможность явным образом указать, какое из свойств папки или сообщения необходимо скопировать или переместить. С **помощью IMAPIProp::CopyTo**, если вы не хотите копировать или перемещать все свойства, необходимо явно указать, какие из них следует исключить. Дополнительные сведения об этих методах см. в сведениях [о копировании свойств MAPI.](copying-mapi-properties.md)
  
Количество скопирований или перемещений свойств может повлиять на принятие решения о том, какой метод использовать. При копировании или перемещении нескольких сообщений вызовите **IMAPIFolder::CopyMessages.** Альтернативным вариантом является вызов **IMAPIProp::CopyProps** для копирования только свойства **PR_CONTAINER_CONTENTS** папки ([PidTagContainerContents).](pidtagcontainercontents-canonical-property.md) В следующей процедуре показано, как **использовать CopyMessages.** 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>Копирование или перемещение одного или более сообщений
  
1. Найдите допустимые идентификаторы записей для исходных и папок назначения.
    
2. Откройте эти папки в режиме чтения и записи, вызывая [IMAPISession::OpenEntry](imapisession-openentry.md) или [IMsgStore::OpenEntry](imsgstore-openentry.md) и устанавливая флаг MAPI_MODIFY. 
    
3. Убедитесь, что указатель интерфейса, возвращаемой **из OpenEntry,** является указателем интерфейса **IMAPIFolder.** Если нет, приведите его к типу LPMAPIFOLDER. 
    
4. Создайте массив идентификаторов записей, представляющих одно или несколько сообщений для копирования или перемещений. 
    
5. Вызовите **IMAPIFolder::CopyMessages** со следующими установленными флагами: 
    
   - MESSAGE_MOVE, если вы хотите выполнить операцию перемещения. 
    
   - MESSAGE_DIALOG и передать окне в  _параметре ulUIParam,_ если необходимо, чтобы в папке был индикатор хода выполнения. 
    
6. **Отпустите указатели IMAPIFolder** для исходных и папок назначения. 
    
Чтобы скопировать все содержимое папки в другую папку, вызовите метод **IMAPIFolder::CopyFolder** или **IMAPIProp::CopyTo** в папке источника. 
  
Чтобы скопировать несколько свойств папки, вызовите метод **IMAPIProp::CopyProps.** Чтобы скопировать большую часть свойств папки, вызовите **IMAPIProp::CopyTo.** 
  
Например, если вы хотите скопировать свойства **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)и **PR_COMMENT** ([PidTagComment),](pidtagcomment-canonical-property.md)у вас есть следующие параметры:
  
- Вызовите **IMAPIFolder::CopyFolder,** чтобы скопировать все свойства папки, а затем удалить ненужные из новой папки. 
    
- Вызовите **CopyTo** и исключить все свойства папки, **кроме** PR_DISPLAY_NAME и **PR_COMMENT.** 
    
- Вызовите **CopyProps,** **передав PR_DISPLAY_NAME** и **PR_COMMENT** в массив include. 
    
В этом случае **copyProps** является лучшим выбором, так как он предназначен для копирования небольшого набора свойств и является самым простым вызовом для реализации. 
  
Чтобы скопировать или переместить только свойства папки, не включая сообщения, вызовите метод **IMAPIProp::CopyTo** папки и исключите следующие свойства: 
  
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)
    
- **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)
    
Методы копирования могут возвращать S_OK, указывая общий успех, MAPI_W_PARTIAL_COMPLETION, обозначая частичный успех или ошибку. Если MAPI_W_PARTIAL_COMPLETION возвращается, используйте **макрос** HR_FAILED для доступа к более конкретной ошибке. Дополнительные сведения см. в теме ["Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)
  
Если вы копируете сообщения из одного хранилище сообщений в другое, и Юникод не поддерживается обоими, следует помнить, что данные могут быть потеряны из-за преобразования страницы кода. Обычно вы не знаете, поддерживают ли в сообщении один или оба формата, что делает невозможным определение того, следует ли копировать текстовые свойства в виде строк ASCII или Юникод. Если вы поддерживаете Юникод, попробуйте выполнить копирование Юникод; В случае с ошибкой со значением ошибки MAPI_E_BAD_CHARWIDTH asCII.
  

