---
title: IMAPIFormInfo IMAPIProp
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
ms.openlocfilehash: 2b2abf4440ee2d81a8e95dcdb5fde2daeaa6e6f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575912"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo : IMAPIProp

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Предоставляет клиентских приложений доступ к свойства для определения формы. Хранение сведений о форме в отдельном объекте, поставщика библиотеки форм можно ввести описание формы в клиент без активации формы.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Предоставляемые:  <br/> |Объекты формы  <br/> |
|Реализованный:  <br/> |Поставщики библиотеки форм  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFormInfo  <br/> |
|Тип указателя:  <br/> |LPMAPIFORMINFO  <br/> |
|Модель транзакций:  <br/> |Не входящих в транзакции  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[CalcFormPropSet](imapiforminfo-calcformpropset.md) <br/> |Возвращает указатель на полный набор свойств, используемых в форме.  <br/> |
|[CalcVerbSet](imapiforminfo-calcverbset.md) <br/> |Возвращает указатель на полный набор команд, которые использует формы.  <br/> |
|[MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) <br/> |Создает значок из свойства значок формы.  <br/> |
|[SaveForm](imapiforminfo-saveform.md) <br/> |Сохраняет описание определенной формы в файл конфигурации.  <br/> |
|[OpenFormContainer](imapiforminfo-openformcontainer.md) <br/> |Возвращает указатель на контейнер формы, в которой установлен определенной формы.  <br/> |
   
## <a name="remarks"></a>Замечания

В отличие от большинства интерфейсы, определенные в файле заголовка MapiForm.h **IMAPIFormInfo** наследует от интерфейса [IMAPIProp](imapipropiunknown.md) , так как экспортирует большинство сведений о форме посредством вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

