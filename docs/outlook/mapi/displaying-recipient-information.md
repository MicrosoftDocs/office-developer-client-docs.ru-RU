---
title: Отображение сведения о получателях
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 7071c05f6f59740163f97f840c7fa48d83bea815
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808329"
---
# <a name="displaying-recipient-information"></a>Отображение сведения о получателях

**Применимо к**: Outlook 
  
MAPI стандартным диалоговым окном служит для отображения сведения о получателе. Диалоговое окно "Подробности" будет создан из таблицы отображения и реализацию **IMAPIProp** . В таблице Отображаемое описание внешний вид отображения сведений и реализации **IMAPIProp** управляет данные для получателя. Поставщик отвечает за предоставление в таблице отображения и реализации **IMAPIProp** для каждого получателя. 
  
Это самый простой способ создания таблицы отображения является определение структуры [DTPAGE](dtpage.md) и вызов [BuildDisplayTable](builddisplaytable.md). Тем не менее некоторые поставщики, а именно только для чтения поставщиков, которые разрешить создание одноразовых получателей используйте **IPropData**. Реализация **IMAPIProp** может иметь любой тип свойства объекта. 
  
Существует два метода для вызова этого диалогового окна: [IAddrBook::Details](iaddrbook-details.md) и [IMAPISupport::Details](imapisupport-details.md). Когда ваш поставщик вызывает один из следующих методов для запроса сведений для получателя, MAPI сначала открывает получателя путем вызова метода [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) его контейнера. Затем вызывается метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) получателя для запроса свойство **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **PR_DETAILS_TABLE** — это свойство, представляющее таблица отображения сведений о получателя. 
  
[IPropData: IMAPIProp](ipropdataimapiprop.md) интерфейс можно использовать для отслеживания изменений для отображения элементов управления в таблице, как описано в следующей процедуре. 
  
## <a name="monitor-changes-to-a-control"></a>Отслеживание изменений для элемента управления
  
1. Прежде чем пользователь получает доступ к элементу управления, вызовите [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) , чтобы задать разрешения доступа IPROP_CLEAN. 
    
2. Предоставление пользователю возможности работы с диалоговое окно. 
    
3. После завершения работы пользователя, вызовите [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) для получения текущего уровня доступа элемента управления. 
    
4. Если уровень доступа IPROP_DIRTY, элемент управления был изменен пользователем. Ваш поставщик выполнить следующие действия:
    
   - Вызовите [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) , чтобы задать доступ уровня вернуться к IPROP_CLEAN. 
    
   - Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) объект данных свойств для извлечения измененное свойство и обновления путем вызова [IMAPIProp::SetProps](imapiprop-setprops.md).
    
5. Если уровень доступа по-прежнему IPROP_CLEAN, элемент управления не был изменен. 
    
Дополнительные сведения о создании таблиц отображения видеть [Отображение таблиц](display-tables.md).
  
