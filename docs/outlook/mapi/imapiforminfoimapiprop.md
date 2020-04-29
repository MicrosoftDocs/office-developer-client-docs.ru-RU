---
title: Имапиформинфо IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3913cb04f1f2f61ba6835b704f430d872756b227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417366"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo : IMAPIProp

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет клиентским приложениям доступ к свойствам, определенным для определения формы. Сохраняя сведения о форме в отдельном объекте, поставщик библиотеки форм может описать форму для клиента, не активируя форму.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиформ. h  <br/> |
|Предоставлено:  <br/> |Объекты сведений о форме  <br/> |
|Реализовано в:  <br/> |Поставщики библиотеки форм  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFormInfo  <br/> |
|Тип указателя:  <br/> |лпмапиформинфо  <br/> |
|Модель транзакции:  <br/> |Не transactd  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[калкформпропсет](imapiforminfo-calcformpropset.md) <br/> |Возвращает указатель на полный набор свойств, которые использует форма.  <br/> |
|[калквербсет](imapiforminfo-calcverbset.md) <br/> |Возвращает указатель на полный набор команд, которые использует форма.  <br/> |
|[макеиконфромбинари](imapiforminfo-makeiconfrombinary.md) <br/> |Создает значок на основе свойства Icon формы.  <br/> |
|[савеформ](imapiforminfo-saveform.md) <br/> |Сохраняет описание конкретной формы в файле конфигурации.  <br/> |
|[опенформконтаинер](imapiforminfo-openformcontainer.md) <br/> |Возвращает указатель на контейнер формы, в котором установлена определенная форма.  <br/> |
   
## <a name="remarks"></a>Примечания

В отличие от большинства интерфейсов, определенных в файле заголовка Мапиформ. h, **имапиформинфо** наследуется от интерфейса [IMAPIProp](imapipropiunknown.md) , так как он экспортирует большинство сведений о форме с помощью вызовов метода [IMAPIProp::-PROPS](imapiprop-getprops.md) . 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

