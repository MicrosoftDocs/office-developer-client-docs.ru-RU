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

**Область применения**: Outlook 2013 | Outlook 2016 
  
MAPI предоставляет общий диалоговое окно для демонстрации сведений о получателе. Диалоговое окно с подробными сведениями создается из таблицы отображения и **реализации IMAPIProp.** В таблице отображения описывается внешний вид отображения сведений, а реализация **IMAPIProp** управляет данными для получателя. Поставщик отвечает за поставку таблицы отображения и **реализацию IMAPIProp** для каждого получателя. 
  
Самый простой способ создания таблицы отображения — определить структуру [DTPAGE](dtpage.md) и вызвать [BuildDisplayTable.](builddisplaytable.md) Однако некоторые поставщики, в частности поставщики только для чтения, которые позволяют создавать разных получателей, используют **IPropData**. Реализация **IMAPIProp может** быть любым типом объекта свойства. 
  
Для этого диалоговое окно можно использовать два метода: [IAddrBook::D etails](iaddrbook-details.md) и [IMAPISupport::D etails](imapisupport-details.md). Когда поставщик вызывает один из этих методов для запроса сведений для получателя, MAPI сначала открывает получателя, вызывая его метод [IMAPIContainer::OpenEntry.](imapicontainer-openentry.md) Далее он вызывает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для запроса **свойства PR_DETAILS_TABLE** [(PidTagDetailsTable).](pidtagdetailstable-canonical-property.md) **PR_DETAILS_TABLE** является свойством, которое представляет таблицу отображения сведений получателя. 
  
Интерфейс [IPropData : IMAPIProp](ipropdataimapiprop.md) можно использовать для мониторинга изменений в элементе управления таблицой отображения, как описано в следующей процедуре. 
  
## <a name="monitor-changes-to-a-control"></a>Отслеживание изменений в области управления
  
1. Прежде чем пользователь получит доступ к нему, позвоните [в IPropData::HrSetObjAccess,](ipropdata-hrsetobjaccess.md) чтобы установить доступ к IPROP_CLEAN. 
    
2. Разрешить пользователю работать с диалоговое окно. 
    
3. Когда пользователь закончит работу, позвоните [в IPropData::HrGetPropAccess,](ipropdata-hrgetpropaccess.md) чтобы получить текущий уровень доступа к данным управления. 
    
4. Если уровень доступа IPROP_DIRTY, пользователь изменил управление. Поставщик должен:
    
   - Вызов [IPropData::HrSetPropAccess,](ipropdata-hrsetpropaccess.md) чтобы установить уровень доступа к IPROP_CLEAN. 
    
   - Чтобы получить измененное свойство и обновить его, позвоните по методу [IMAPIProp::GetProps](imapiprop-getprops.md) объекта [IMAPIProp::SetProps.](imapiprop-setprops.md)
    
5. Если уровень доступа по-прежнему IPROP_CLEAN, управление не было изменено. 
    
Дополнительные сведения о создании таблиц отображения см. в таблице [Display Tables.](display-tables.md)
  

