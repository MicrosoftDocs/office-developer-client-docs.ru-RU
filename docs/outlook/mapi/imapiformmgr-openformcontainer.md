---
title: IMAPIFormMgrOpenFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 68a358c91e35c5a075e220794c78f4e5c96e43ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321639"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает интерфейс [IMAPIFormContainer](imapiformcontaineriunknown.md) для определенного контейнера формы. 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Параметры

 _hfrmreg_
  
> [in] Enumeration HFRMREG that indicates the form library to open (that is, the form container to open). Enumeration HFRMREG — это enumeration, специфичной для поставщика библиотеки форм. Возможные значения HFRMREG:
    
HFRMREG_DEFAULT 
  
> Удобный контейнер формы.
    
HFRMREG_FOLDER 
  
> Контейнер папок. 
    
HFRMREG_PERSONAL 
  
> Контейнер для хранения сообщений по умолчанию. 
    
HFRMREG_LOCAL 
  
> Локальный контейнер формы. 
    
 _lpunk_
  
> [in] Указатель на объект, для которого открыт интерфейс. Параметр  _lpunk_ должен иметь значение **NULL,** если для значения  _параметра hfrmreg_ не требуется указатель объекта. 
    
 _lppfcnt_
  
> [out] Указатель на указатель на возвращенный объект контейнера формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_INTERFACE 
  
> Объект, на который указывает  _lpunk,_ не поддерживает необходимый интерфейс. 
    
## <a name="remarks"></a>Примечания

Посетители форм звонят **методу IMAPIFormMgr::OpenFormContainer,** чтобы открыть **интерфейс IMAPIFormContainer** для определенного контейнера формы. Затем этот интерфейс можно использовать для установки форм и удаления форм из контейнера форм. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если значение в _hfrmreg_ HFRMREG_FOLDER, идентификатор интерфейса, используемый в _lpunk,_ должен быть ненулев и разрешит вызовы метода [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) к интерфейсу [IMAPIFolder.](imapifolderimapicontainer.md)  
  
Чтобы открыть локальный контейнер формы, необходимо использовать вызов метода **OpenFormContainer** или функции [MAPIOpenLocalFormContainer;](mapiopenlocalformcontainer.md) Вы не можете использовать метод [IMAPIFormMgr::SelectFormContainer,](imapiformmgr-selectformcontainer.md) чтобы позволить пользователю выбрать локальный контейнер формы. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenFormContainer  <br/> |MFCMAPI использует метод **IMAPIFormMgr::OpenFormContainer** для получения контейнера формы, чтобы можно было отрисовывать содержимое контейнера.  <br/> |
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnOpenFormContainer  <br/> |MFCMAPI использует метод **IMAPIFormMgr::OpenFormContainer** для получения контейнера формы для папки, чтобы можно было отрисовывать содержимое контейнера.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

