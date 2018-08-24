---
title: IProviderAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0f917989d9bac403f2bea5b2d6699b7a1caf2008
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573014"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает профиля из текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшей доступа. 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>Параметры

 _lpUID_
  
> [in] Указатель на структуру [MAPIUID](mapiuid.md) , который содержит уникальный идентификатор для профиля раздел, чтобы открыть. Клиенты не должны передать значение NULL для параметра _lpUID_ . Поставщиков услуг можно передать значение NULL для получения **MAPIUID** , когда он совершает вызов из их функций точки входа службы сообщения. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к раздела профиля. В разделе профиль стандартный интерфейс (**IProfSect**), возвращаемых результатов передаче значения NULL. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который управляет способа открытия раздела профиля. Можно задать следующие флажки:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenProfileSection** для возврата успешно, возможно до раздела профиля доступными для вызывающего абонента. Если в разделе профиль не поддерживается, последующие подключения к нему может вызвать ошибку. 
    
MAPI_MODIFY 
  
> Запросы на разрешение чтения и записи. По умолчанию объекты открываются с разрешением только для чтения и звонящие не должны работать предполагается, что что назначено разрешение чтения и записи. Клиенты не разрешены разрешение на чтение и запись к разделам поставщика профиля.
    
MAPI_FORCE_ACCESS
  
> Разрешает доступ всех разделах профилей, даже теми, поставщиками отдельные службы.
    
 _lppProfSect_
  
> [out] Указатель на указатель на раздел профилей.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> В разделе профилей успешно открыт.
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка изменения раздела профиля только для чтения или для доступа к объекту, для которого пользователь имеет недостаточно разрешений.
    
MAPI_E_NOT_FOUND 
  
> В разделе запрошенные профиля не существует.
    
## <a name="remarks"></a>Замечания

Метод **IProviderAdmin::OpenProfileSection** открывает раздел профилей, включение вызывающего абонента для чтения данных из и возможно записи сведений о текущей конфигурации. 
  
Клиенты не могут открывать профилей разделов, относящихся к поставщиков с помощью метода **OpenProfileSection** . 
  
Несколько клиентов или поставщиков услуг можно одновременно открыть профиля с разрешением только для чтения. Тем не менее при открытии получившие разрешение на чтение и запись профиля нет других вызовов невозможны откройте раздел, независимо от типа доступа. Если раздел профилей открыт с разрешением только для чтения, следующий вызов метода, запрашивающих разрешение на чтение и запись завершится с MAPI_E_NO_ACCESS. Аналогичным образом Если раздел открыт с разрешением на чтение и запись, следующий вызов метода, запрашивающих разрешение на чтение также не будет работать. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если запрос, который **OpenProfileSection** открыть несуществующий профиля, передав MAPI_MODIFY в _ulFlags_ и будет создана Неизвестная **MAPIUID** в _lpUID_, в разделе профилей. 
  
При запросе, **OpenProfileSection** открыть несуществующий раздел с разрешением только для чтения, возвращает MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |Mfcmapi (en) использует метод **IProviderAdmin::OpenProfileSection** для открытия профиля из текущего профиля.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

