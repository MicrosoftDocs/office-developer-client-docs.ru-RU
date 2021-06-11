---
title: IMAPIFormMgrSelectFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bfddc24e6a9c7cf8bdeae1e5ea730ecdb116f564
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428594"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Представляет диалоговое окно, которое позволяет пользователю выбрать контейнер формы и возвращает интерфейс для выбранного пользователем объекта контейнера.
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна отображаемого диалогового окна. 
    
 _ulFlags_
  
> [in] Битмаска флагов, которая управляет тем, как выбирается библиотека форм (то есть, как выбирается контейнер формы). Можно установить следующие флаги:
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> Выбор можно сделать из всех контейнеров. Это тип выбора по умолчанию. 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> Выбор можно сделать только из контейнеров папок.
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> Выбор может быть выполнен только из контейнеров, не связанных с папками.
    
 _lppfcnt_
  
> [вышел] Указатель на указатель на возвращенный интерфейс. Этот интерфейс для объекта контейнера, выбранного пользователем.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Как правило, зрители формы звонят по **методу IMAPIFormMgr::SelectFormContainer,** чтобы выбрать контейнер формы, в который установлена форма. **SelectFormContainer** нельзя использовать для выбора локального контейнера форм, который имеет значение HFRMREG_LOCAL. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSelectFormContainer  <br/> |MFCMAPI использует **метод IMAPIFormMgr::SelectFormContainer** для выбора контейнера формы перед отрисовка его содержимого.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

