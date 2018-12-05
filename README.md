# CaBMI_2D
Repo for 2D BMI analysis, data pointing, and figure generation


### Pre-flight
Dependencies: [CaBMI Repo](https://github.com/WALIII/CaBMI)

### Editable Manuscript
[Neuroprosthetic navigation of a 2D soundscape](https://docs.google.com/document/d/1syMSfIxXzNNJ4ZskQphiOOgFsW8hd29XXnzQHSpKUEA/edit)



## 1. Folder Contents

```
% ROI DATA %
ave_roi.mat              % Indirect neurons during BMI experiment
Direct_roi.mat           % Direct Neurons during BMI experiment
Indirect_roi_map.mat     % Baseline activity of Indirect neurons
Direct_roi_map.mat       % Baseline activity of Direct Neurons


% ADDITIONAL DATA %
csv_data.mat             % reward alignment data
Y.mat                    % Aligned raw video            
```

### Analysis Run through:



## 1. Index into 'processed' folder for one animal. Load in ROI data:
```
>> CaBMI2D_PreFlight
```


##  Basic Extraction of 'Hits' from .CSV file
```
>> [ds_hits, roi_hits] = CaBMI_csvAlign(csv_data(:,2),csv_data(:,3),roi_ave1); %   1. Load in Y ( temporally downsampled movie) from ds_data


% Get ROI traces in a matrix, bounded by the hits
>> [ROIhits, ROIhits_d, ROIhits_s, ROIhits_z]= CaBMI_getROI(roi_ave1,roi_hits);

% Get ROI traces for DIRECT neurons...
>> [D_ROIhits, D_ROIhits_d, D_ROIhits_s, D_ROIhits_z]= CaBMI_getROI(roi_ave2,roi_hits);
```
