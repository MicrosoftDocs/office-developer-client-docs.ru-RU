---
title: IAddrBookGetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetSearchPath
api_type:
- COM
ms.assetid: 43b51a66-71fa-4e10-93e4-d533b48af4de
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f8c129e772870804ef464765b2035a3582317a09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412984"
---
# <a name="iaddrbookgetsearchpath"></a>IAddrBook::GetSearchPath

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает упорядоченный список идентификаторов записей контейнеров, которые необходимо включить в процесс разрешения имен, инициированный методом [IAddrBook::ResolveName.](iaddrbook-resolvename.md) 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом строк, возвращаемого в пути поиска. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Возвращенные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
 _lppSearchPath_
  
> [out] Указатель на указатель на упорядоченный список идентификаторов записей контейнера. **GetSearchPath** сохраняет упорядоченный список в [структуре SRowSet.](srowset.md) Если в иерархии адресной книги нет контейнеров, в структуре **SRowSet** возвращается ноль. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Путь поиска был успешно извлечен.
    
## <a name="remarks"></a>Примечания

Клиенты и поставщики услуг вызвать метод **GetSearchPath,** чтобы получить путь поиска, используемый для разрешения имен с помощью метода **ResolveName.** Обычно клиенты звонят [методу IAddrBook::SetSearchPath,](iaddrbook-setsearchpath.md) чтобы установить путь поиска контейнера в профиле, прежде чем вызывать **GetSearchPath для** его извлечения. Однако вызов **SetSearchPath является необязательным.** 
  
Если **SetSearchPath** никогда не был вызван, **GetSearchPath** создает путь, проработав таблицы иерархии адресной книги. Путь поиска по умолчанию, установленный **GetSearchPath,** состоит из следующих контейнеров в следующем порядке: 
  
1. Первый контейнер с разрешением на чтение и записи, обычно это личная адресная книга (PAB).
    
2. Каждый контейнер, **для свойства PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)установлено DT_GLOBAL. Этот параметр указывает, что контейнер содержит получателей. 
    
3. Контейнер, назначенный в качестве контейнера по умолчанию, если в свойстве  PR_DISPLAY_TYPE нет контейнеров с флагом DT_GLOBAL, а контейнер по умолчанию отличается от первого контейнера с разрешением на чтение и записи. 
    
Если **метод SetSearchPath** был вызван, **Метод GetSearchPath** создает путь с помощью контейнеров адресной книги, сохраненных в профиле. **GetSearchPath** проверяет этот путь, прежде чем возвращать его вызываемой. 
  
После первого вызова **SetSearchPath** последующие вызовы **SetSearchPath** должны использоваться для изменения пути поиска, возвращаемой **GetSearchPath.** Другими словами, вызываемому клиенту или поставщику не будет назначен путь поиска по умолчанию после первого вызова **SetSearchPath.**
  
## <a name="see-also"></a>См. также



[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

