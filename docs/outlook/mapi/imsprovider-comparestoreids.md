---
title: Имспровидеркомпарестореидс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 734e53c1e897c902c72319aa6f2d3d7af2d23fb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431710"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сравнивает два идентификатора записи хранилища сообщений, чтобы определить, ссылаются ли они на один и тот же объект хранилища.
  
```cpp
HRESULT CompareStoreIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID1_
  
> возврата Размер (в байтах) идентификатора записи, на который указывает параметр _lpEntryID1_ _._
    
 _lpEntryID1_
  
> возврата Указатель на первый идентификатор записи, который необходимо сравнить.
    
 _cbEntryID2_
  
> возврата Размер (в байтах) идентификатора записи, на который указывает параметр _lpEntryID2_ _._
    
 _lpEntryID2_
  
> возврата Указатель на второй идентификатор записи, который необходимо сравнить.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _Лпулресулт_
  
> вышли Указатель на возвращаемый результат сравнения. ЗНАЧЕНИЕ TRUE, если два идентификатора записи ссылаются на один объект; в противном случае — FALSE.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

MAPI вызывает метод **функцииimsprovider:: компарестореидс** при обработке вызова метода [IMAPISession:: опенмсгсторе](imapisession-openmsgstore.md) . В этой точке вызывается **компарестореидс** , чтобы определить, какой раздел профиля связан с открываемым хранилищем сообщений. Вызов **компарестореидс** можно выполнить, если нет открытых хранилищ сообщений для конкретного поставщика услуг хранения. Кроме того, MAPI также вызывает **компарестореидс** , когда он обрабатывает вызов поставщика хранилища в метод [Имаписуппорт:: опенпрофилесектион](imapisupport-openprofilesection.md) . 
  
Идентификаторы записей, по сравнению с **компарестореидс** , предназначены для библиотеки динамической КОМПОНОВКИ (DLL) текущего поставщика хранилища (DLL) и являются неупакованными идентификаторами записей в хранилище. Дополнительные сведения о переносе идентификаторов записей в хранилище можно найти в статье [имаписуппорт:: врапсторинтрид](imapisupport-wrapstoreentryid.md).
  
Возможность сравнения идентификаторов записей полезна, так как объект может иметь несколько допустимых идентификаторов записей. Это может произойти, например, после установки новой версии поставщика хранилища сообщений. 
  
## <a name="see-also"></a>См. также



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

