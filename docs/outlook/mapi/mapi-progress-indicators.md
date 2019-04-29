---
title: Индикаторы хода выполнения MAPI
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
# <a name="mapi-progress-indicators"></a>Индикаторы хода выполнения MAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Многие операции, выполняемые для клиентов, могут занимать много времени. Чтобы уведомить клиентов о ходе выполнения длительной операции, можно отобразить индикатор, отображающий законченную часть операции в любой заданную точку от начала операции до ее завершения. Индикатор выполнения показывает процент от общей операции, которую необходимо выполнить.
  
Следующие методы поддерживают длительные операции и отображают индикатор хода выполнения:
  
- [IMAPIFolder:: копимессажес](imapifolder-copymessages.md), [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D Елетемессажес](imapifolder-deletemessages.md), [IMAPIFolder::D Елетефолдер](imapifolder-deletefolder.md), [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md)и [IMAPIFolder:: сетреадфлагс](imapifolder-setreadflags.md).
    
- [IMAPIProp:: копипропс](imapiprop-copyprops.md) и [IMAPIProp:: CopyTo](imapiprop-copyto.md).
    
- [Имаписуппорт::D окопипропс](imapisupport-docopyprops.md), [Имаписуппорт::D окопито](imapisupport-docopyto.md), [Имаписуппорт:: CopyFolder](imapisupport-copyfolder.md)и [имаписуппорт:: копимессажес](imapisupport-copymessages.md).
    
- [IMessage::D елетеаттач](imessage-deleteattach.md).
    
- [Иабконтаинер:: копентриес](iabcontainer-copyentries.md).
    
Чтобы отобразить индикатор хода выполнения, MAPI определяет объект хода выполнения. Объекты хода выполнения реализуют интерфейс [IMAPIProgress: IUnknown](imapiprogressiunknown.md) , интерфейс, который включает методы для установки диапазона индикатора и создания отображения. MAPI предоставляет реализацию объекта Progress, как и некоторые клиенты. Следует использовать реализацию клиента, если она предоставляется в качестве входного параметра для метода, выполняющего операцию. Если клиент передает значение NULL, а не указатель на объект Progress, используйте реализацию MAPI, вызвав метод [имаписуппорт::D опрогрессдиалог](imapisupport-doprogressdialog.md) . 
  
## <a name="see-also"></a>См. также



[Поставщики службы MAPI](mapi-service-providers.md)

