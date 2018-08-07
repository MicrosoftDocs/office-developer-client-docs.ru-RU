---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e693e1c3d6cb975a3a329e15c0b1a6d08817461a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808724"
---
# <a name="iablogonopenstatusentry"></a>IABLogon::OpenStatusEntry

  
  
**Относится к**: Outlook 
  
Открывает объект состояние поставщика.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a>Параметры

 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который должен использоваться для доступа к объекту состояния. Передача NULL возвращает объект стандартный интерфейс, [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет способ открытия объекта состояния. Можно задать следующий флаг:
    
MAPI_MODIFY 
  
> Запросы на разрешение чтения и записи. По умолчанию объекты открываются с доступом только для чтения и абонентов не следует предполагать, что предоставлены разрешения на чтение и запись.
    
 _lpulObjType_
  
> [out] Указатель на тип объекта открыт.
    
 _lppEntry_
  
> [out] Указатель на указатель на объект открыт.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов завершился успешно и открытия объекта состояния.
    
## <a name="remarks"></a>Замечания

Метод **OpenStatusEntry** , чтобы предоставить доступ к их состояние объекта, реализуемые поставщиками адресных книг. Все поставщиками адресной книги необходимы для реализации объект состояния, который поддерживает как минимум, метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . Для получения дополнительных сведений см [Реализация объекта состояния](status-object-implementation.md).
  
## <a name="see-also"></a>См. также



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

