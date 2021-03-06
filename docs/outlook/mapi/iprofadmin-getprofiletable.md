---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2db7dba67e7b71df6921ecd97189255a0ef7823a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414648"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице профилей, таблице, содержаной сведения обо всех доступных профилях.
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Всегда NULL.
    
 _lppTable_
  
> [вышел] Указатель на указатель на таблицу профилей.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица профилей была успешно извлечена.
    
## <a name="remarks"></a>Примечания

Метод **IProfAdmin::GetProfileTable** предоставляет доступ к таблице профилей, которая содержит одну строку для каждого доступного профиля. В каждой строке есть только два столбца: имя отображения профиля и флаг, который указывает, является ли профиль по умолчанию. 
  
Профили, которые были удалены или используются, но помечены для удаления, не включаются в таблицу профилей. Таблица профилей статична; последующие добавления и удаления профилей не отражаются в таблице. 
  
Если профили не существуют, **GetProfileTable** возвращает таблицу с нулевыми строками. 
  
Дополнительные сведения о таблице профилей см. в таблице ["Таблицы профилей".](profile-tables.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnShowProfiles  <br/> |MFCMAPI использует **метод IProfAdmin::GetProfileTable** для отображения таблицы профилей в новом диалоговом окне.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

