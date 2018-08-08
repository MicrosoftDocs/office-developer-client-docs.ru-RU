---
title: Индикаторы выполнения MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d8af2ba3067dabe759056313eb278b9901510980
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809797"
---
# <a name="mapi-progress-indicators"></a>Индикаторы выполнения MAPI

  
  
**Относится к**: Outlook 
  
Многие из операций, выполняемых для клиентов, может занять много времени. Информирование клиентов о ходе выполнения длительной операции, можно отобразить индикатор, который отображает графическое по завершении работы часть операции в данный момент от начала операции до его завершения. Индикатор показывает процент завершения общее операции.
  
Следующие методы поддерживают длительных операций и отображение индикатора хода выполнения.
  
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)и [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md) и [IMAPIProp::CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)и [IMAPISupport::CopyMessages](imapisupport-copymessages.md).
    
- [IMessage::DeleteAttach](imessage-deleteattach.md).
    
- [IABContainer::CopyEntries](iabcontainer-copyentries.md).
    
Чтобы отобразить индикатор выполнения, MAPI определяет объект хода выполнения. Объекты хода выполнения реализовать [IMAPIProgress: IUnknown](imapiprogressiunknown.md) интерфейса, интерфейс, который содержит методы для создания диапазона индикатора и создание отображения. MAPI предоставляет реализацию объекта о ходе выполнения, как и некоторыми клиентами. Реализация клиента, следует использовать, если оно предоставлено, как входного параметра для метода для выполнения операции. Если клиент передает значение NULL вместо указателя на объект ход выполнения, описание использования реализации интерфейса MAPI путем вызова метода [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) . 
  
## <a name="see-also"></a>См. также



[Поставщиков служб MAPI](mapi-service-providers.md)

