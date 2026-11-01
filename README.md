# Approach-Avoidance Conflict Task (AACT)

An OpenSesame implementation of the Approach-Avoidance Conflict Task (AACT), designed to investigate approach-avoidance behavior when decisions involve both rewarding and aversive outcomes.

## Sound Calibration

Before starting the task, participants complete a two-step sound calibration procedure:

1. **Comfortable listening level:** Participants listen to a spoken story and adjust the volume to a comfortable listening level.
2. **Aversive listening level:** Participants listen to an aversive sound and adjust the volume until it is noticeably unpleasant but still tolerable, without risking hearing damage.

## Task Description

Participants are presented with a choice between approaching an aversive stimulus to receive points or avoiding it and receiving no reward.

- **Approach:** The participant receives points but is exposed to an aversive image and sound.
- **Avoid:** The participant receives no points and is presented with a neutral image and sound.

Each trial consists of four stages:

1. **Reward rating:** Participants rate how much they desire the points offered.
2. **Expected aversiveness:** Participants rate how unpleasant they expect the image and sound to be.
3. **Decision:** Participants choose whether to approach or avoid the aversive stimulus.
4. **Experienced aversiveness:** After the image and sound are presented, participants rate how unpleasant the experience was.

At the end of the experiment, participants are shown the total number of points they accumulated.

## Task Structure

The experiment consists of:

- 3 practice trials.
- 8 experimental trials.

The practice trials familiarize participants with the procedure before beginning the experimental trials.

## Language

The experiment instructions are in Swedish.

## Stimuli

The experiment uses aversive and neutral images accompanied by corresponding sounds.

**Image stimuli are not included in this repository due to copyright restrictions.** Users must provide their own appropriately licensed images before running the experiment.

The images must follow the naming convention expected by the experiment.

### Experimental Stimuli

| Stimulus type | Filenames                                  | Number of images |
| ------------- | ------------------------------------------ | ---------------- |
| Aversive      | `aversive_1.jpg` through `aversive_16.jpg` | 16               |
| Neutral       | `neutral_1.jpg` through `neutral_16.jpg`   | 16               |

### Practice Stimuli

The practice trials use separate images identified by the suffix `B`.

```text
aversive_1B.jpg
aversive_2B.jpg
aversive_3B.jpg

neutral_1B.jpg
neutral_2B.jpg
neutral_3B.jpg
```

A total of 38 image files are expected across both stimulus categories.

Replacement images must use the specified filenames to match the experiment's references.

## Participant Identification

The experiment is designed to run through JATOS and retrieves the participant ID (`pid`) from the URL query parameters.

```javascript
vars.ID = jatos.urlQueryParameters.pid;
```

For example, if the experiment is launched with:

`https://example.com/study?pid=1234`

Then `vars.ID` will contain `"1234"`.

When running the experiment without JATOS, the reference to `jatos.urlQueryParameters` should be removed or replaced to avoid errors.
