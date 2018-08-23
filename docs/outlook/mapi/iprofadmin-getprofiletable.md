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
ms.openlocfilehash: 8b1b037cf24c1bb5a0c84da3d59892ab15763f37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588246"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице профилей таблицу, содержащую сведения обо всех доступных профилей.
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Всегда имеет значение NULL.
    
 _lppTable_
  
> [out] Указатель на указатель в таблице профилей.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> В таблице профиль был успешно извлечен.
    
## <a name="remarks"></a>Замечания

Метод **IProfAdmin::GetProfileTable** предоставляет доступ к таблице профиля, который содержит одну строку для всех доступных профилей. В каждой строке есть только два столбца: отображаемое имя профиля и флаг, указывающий, является ли профиль по умолчанию. 
  
Профили, которые были удалены или используются, однако помечены для удаления, не включаются в таблице профилей. В таблице профилей является статическим. последующие добавления и удаления профилей, не отражаются в таблице. 
  
Если профили не существует, **GetProfileTable** возвращает таблицу с нуля строк. 
  
Дополнительные сведения о таблице профилей см [Профиля](profile-tables.md). 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnShowProfiles  <br/> |Mfcmapi (en) использует метод **IProfAdmin::GetProfileTable** для получения профиля таблицу для отображения в диалоговом окне новый.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

