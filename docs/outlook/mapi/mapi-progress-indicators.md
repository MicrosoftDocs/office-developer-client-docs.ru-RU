---
title: Индикаторы прогресса MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cdfb6898146583b7da9b043eadd3acc09edbf292
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410709"
---
# <a name="mapi-progress-indicators"></a>Индикаторы прогресса MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Выполнение многих операций для клиентов может занять много времени. Чтобы информировать клиентов о ходе длительной операции, можно показать индикатор, который графически отображает готовую часть операции в любой момент от начала операции до ее завершения. Индикатор прогресса показывает процент от общей операции, которая должна быть выполнена.
  
Следующие методы поддерживают длительные операции и отображение индикатора прогресса:
  
- [IMAPIFolder::CopyMessages,](imapifolder-copymessages.md) [IMAPIFolder::CopyFolder,](imapifolder-copyfolder.md) [IMAPIFolder::D eleteMessages,](imapifolder-deletemessages.md) [IMAPIFolder::D eleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md) и [IMAPIProp::CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::D oCopyProps,](imapisupport-docopyprops.md) [IMAPISupport::D oCopyTo,](imapisupport-docopyto.md) [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)и [IMAPISupport::CopyMessages](imapisupport-copymessages.md).
    
- [IMessage::D eleteAttach](imessage-deleteattach.md).
    
- [IABContainer::CopyEntries](iabcontainer-copyentries.md).
    
Чтобы отобразить индикатор прогресса, MAPI определяет объект прогресса. Объекты progress реализуют [интерфейс IMAPIProgress : IUnknown,](imapiprogressiunknown.md) интерфейс, который включает методы для установления диапазона индикатора и создания дисплея. MAPI обеспечивает реализацию объекта progress, как и некоторые клиенты. При его поставке необходимо использовать реализацию клиента в качестве параметра ввода метода выполнения операции. Если клиент передает NULL вместо указателя на объект прогресса, используйте реализацию MAPI, позвонив [методу IMAPISupport::D oProgressDialog.](imapisupport-doprogressdialog.md) 
  
## <a name="see-also"></a>См. также



[Поставщики услуг MAPI](mapi-service-providers.md)

