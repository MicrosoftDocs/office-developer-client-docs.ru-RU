---
title: Отображение сведений о получателях
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e1c31e5edf702dd8f172f67e7055a96ae4cfff1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412957"
---
# <a name="displaying-recipient-information"></a>Отображение сведений о получателях

**Относится к**: Outlook 2013 | Outlook 2016 
  
MAPI предоставляет общее диалоговое окно для показа сведений о получателе. Диалоговое окно сведений создается из таблицы отображения и реализации **IMAPIProp.** В таблице отображения описывается внешний вид отображения сведений, а реализация **IMAPIProp** управляет данными для получателя. Поставщик отвечает за отображение таблицы и **реализацию IMAPIProp** для каждого получателя. 
  
Самый простой способ создать таблицу отображения — определить [структуру DTPAGE](dtpage.md) и вызвать [BuildDisplayTable.](builddisplaytable.md) Однако некоторые поставщики, в частности поставщики, предназначенные только для чтения, которые позволяют создавать отдельных получателей, используют **IPropData.** Реализацией **IMAPIProp** может быть любой тип объекта свойства. 
  
Существует два метода для этого диалоговых окна: [IAddrBook::D etails](iaddrbook-details.md) и [IMAPISupport::D etails](imapisupport-details.md). Когда поставщик вызывает один из этих методов для запроса сведений о получателе, MAPI сначала открывает получателя, вызывая метод [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) его контейнера. Затем он вызывает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) получателя, чтобы запросить **свойство PR_DETAILS_TABLE** ([PidTagDetailsTable).](pidtagdetailstable-canonical-property.md) **PR_DETAILS_TABLE** это свойство, которое представляет таблицу отображения сведений получателя. 
  
Интерфейс [IPropData : IMAPIProp](ipropdataimapiprop.md) можно использовать для отслеживания изменений элементов управления таблицы отображения, как описано в следующей процедуре. 
  
## <a name="monitor-changes-to-a-control"></a>Отслеживание изменений в контроле
  
1. Прежде чем пользователь получит доступ к нему, вызовите [IPropData::HrSetObjAccess,](ipropdata-hrsetobjaccess.md) чтобы установить доступ к IPROP_CLEAN. 
    
2. Разрешить пользователю работать с диалогом. 
    
3. Когда пользователь завершит работу, вызовите [IPropData::HrGetPropAccess,](ipropdata-hrgetpropaccess.md) чтобы получить текущий уровень доступа к нему. 
    
4. Если уровень доступа IPROP_DIRTY, пользователь изменил его. Поставщик должен:
    
   - Вызовите [IPropData::HrSetPropAccess,](ipropdata-hrsetpropaccess.md) чтобы вернуть уровень доступа к IPROP_CLEAN. 
    
   - Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) объекта данных свойства, чтобы получить измененное свойство и обновить его, вызывая [IMAPIProp::SetProps.](imapiprop-setprops.md)
    
5. Если уровень доступа по-прежнему IPROP_CLEAN, то этот контроль не был изменен. 
    
Дополнительные сведения о создании таблиц отображения см. в [таблице отображения.](display-tables.md)
  

